---
layout: default-layout
title: Scan & Parse Passport - Dynamsoft Capture Vision iOS Edition
description: This page introduce how to scan and parse a passport with Dynamsoft Capture Vision iOS Edition.
keywords: iOS, passport
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# iOS User Guide for Passport Integration

## Requirements

- Supported OS: iOS 11+ (iOS 13+ recommended).
- Supported ABI: arm64 and x86_64.
- Development Environment: Xcode 13+ (Xcode 14.1+ recommended).

## Add the Libraries

To build the passport application, it is essential to integrate the following libraries from the Dynamsoft Capture Vision SDK:

   | File | Description |
   |---------|-------------|
   | `DynamsoftCaptureVisionRouter.xcframework` | The Dynamsoft Capture Vision Router module is the cornerstone of the Dynamsoft Capture Vision (DCV) architecture. It focuses on coordinating batch image processing and provides APIs for setting up image sources and result receivers, configuring workflows with parameters, and controlling processes. |
   | `DynamsoftLabelRecognizer.xcframework` | The Dynamsoft Label Recognizer module identifies and recognizes text labels such as passport MRZs, ID cards, and VIN numbers. |
   | `DynamsoftCore.xcframework` | The Dynamsoft Core module lays the foundation for Dynamsoft SDKs based on the DCV (Dynamsoft Capture Vision) architecture. It encapsulates the basic classes, interfaces, and enumerations shared by these SDKs. |
   | `DynamsoftImageProcessing.xcframework` | The Dynamsoft Image Processing module facilitates digital image processing and supports operations for other modules, including the Barcode Reader, Label Recognizer, and Document Normalizer.  |
   | `DynamsoftNeuralNetwork.xcframework` | The Dynamsoft Neural Network module allows SDKs compliant with the DCV (Dynamsoft Capture Vision) architecture to leverage the power of deep learning when processing digital images. |
   | `DynamsoftLicense.xcframework` | The Dynamsoft License module manages the licensing aspects of Dynamsoft SDKs based on the DCV (Dynamsoft Capture Vision) architecture. |
   | `DynamsoftCameraEnhancer.xcframework` | The <a href="/camera-enhancer/docs/mobile/programming/ios/" target="_blank">Dynamsoft Camera Enhancer (DCE) module</a> controls the camera, transforming it into an image source for the DCV (Dynamsoft Capture Vision) architecture through ISA implementation. It also enhances image quality during acquisition and provides basic viewers for user interaction. |
   | `DynamsoftUtility.xcframework` | The Dynamsoft Utility module defines auxiliary classes, including the ImageManager, and implementations of the CRF (Captured Result Filter) and ISA (Image Source Adapter). These are shared by all Dynamsoft SDKs based on the DCV (Dynamsoft Capture Vision) architecture.|
   | `DynamsoftCodeParser.xcframework` | The Dynamsoft Code Parser module converts data strings, typically encrypted in barcodes and machine-readable zones, into human-readable information. |
   | `DynamsoftCodeParserDedicator.xcframework` | The Dynamsoft Code Parser Dedicator module provides auxiliary functionality to enhance and extend the capabilities of DCP module. |

1. Add the frameworks in your **Podfile**, replace *TargetName* with your real target name.

    ```pod
    target '{Your project name}' do
        use_frameworks!

        pod 'DynamsoftLabelRecognizerBundle','3.2.3000'
        pod 'DynamsoftCodeParser','2.2.10'
        pod 'DynamsoftCodeParserDedicator','1.2.20'

    end
    ```

2. Execute the pod command to install the frameworks and generate workspace(**{Your project name}.xcworkspace**):

   ```bash
   pod install
   ```

## Build Your First Application

In this section, we will explain how to create a `HelloWorld` implementation similar to our simple `PassportScanner` app for reading the MRZ zone from camera video input.

>Note:
>
>- The following steps are completed in XCode 14.2
>- You can get similar source code from <a href="https://github.com/Dynamsoft/passport-mrz-scanner-mobile/tree/main/ios/PassportMRZScanner" target="_blank">PassportScanner Sample(Swift)</a>

### Create a New Project

1. Open XCode and select *Create a new Xcode Project* or in the *File > New > Project* menu to create a new project.

2. Select **iOS -> App** for your application.

3. Input your product name (HelloWorld), interface (StoryBoard) and language (Swift)

4. Click on **Next** and select the location to save the project.

5. Click on **Create** to finish  creating the new project.

### Include the Library

To add the SDK to your new project, please read [Add the Libraries](#add-the-libraries) section for more details.

### Deploy the CharacterModel & Template

A `CharacterModel` is a model file trained using deep neural networks for character recognition. A `Template` file in the Dynamsoft Capture Vision SDK offers a customizable configuration for optimizing barcode recognition, label recognition, document normalization, and bytes parsing settings. This enables users to tailor the capture process to their specific needs. For passport scanning, you have to include the required the MRZ `CharacterModel` and `Template` in your project first.

1. Create a **DynamsoftResources** folder in the finder. Under the **DynamsoftResources** folder create two new folders, **CharacterModel** and **Templates**.

2. Copy the <a href="https://cdn.jsdelivr.net/npm/dynamsoft-label-recognizer-data@1.0.11/dist/MRZ.data" target="_blank">**MRZ.data**</a> to the `CharacterModel` folder.

3. Copy your template file <a href="https://github.com/Dynamsoft/passport-mrz-scanner-mobile/blob/main/ios/PassportMRZScanner/DynamsoftResources.bundle/Templates/PassportScanner.json" target="_blank">**PassportScanner.json**</a> to the **Templates** folder.

4. Rename the **DynamsoftResources** folder's extension name to **.bundle** and drag the **DynamsoftResources.bundle** into your project on Xcode. Select **Create groups** for the **Added folders** option.



### Initialize the License

1. Use the `LicenseManager` class and initialize the license in **AppDelegate**.

    ```swift
    import DynamsoftLicense
    class AppDelegate: UIResponder, UIApplicationDelegate, LicenseVerificationListener {
        func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
            LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", verificationDelegate:self)
            return true
        }
        func onLicenseVerified(_ isSuccess: Bool, error: Error?) {
            if(error != nil)
            {
                if let msg = error?.localizedDescription {
                    print("Server license verify failed, error:\(msg)")
                }
            }
        }
    }
    ```

   >Note:  
   >
   >- The license string here grants a time-limited free trial which requires network connection to work.
   >- You can request for a 30-day trial license via the <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=passport&utm_source=docs&package=ios" target="_blank">Trial License link</a>. Offline trial license is also available by <a href="https://www.dynamsoft.com/contact/" target="_blank">contacting us</a>.

### Initialize the Camera Module

Create the instances of `CameraEnhancer` and `CameraView` in **ViewController**.

```swift
import DynamsoftCameraEnhancer
...
class ViewController: UIViewController {
    private var dce: CameraEnhancer!
    private var dceView: CameraView!
    private var dlrDrawingLayer: DrawingLayer!

    private func configureDCE() -> Void {
        dceView = .init(frame: view.bounds)
        dceView.scanLaserVisible = true
        dceView.autoresizingMask = [.flexibleWidth, .flexibleHeight]
        self.view.addSubview(dceView)
        
        dlrDrawingLayer = dceView.getDrawingLayer(DrawingLayerId.DLR.rawValue)
        dlrDrawingLayer!.visible = true
        dce = CameraEnhancer(view: dceView)
        dce.enableEnhancedFeatures(.frameFilter)
   }
}
```

### Initialize the Capture Vision Router

Create an instance of `CaptureVisionRouter` and bind it with the already created instance of `DynamsoftCameraEnhancer`.

```swift
import DynamsoftCaptureVisionRouter
...
class ViewController: UIViewController {
    private var cvr: CaptureVisionRouter!
    private var resultFilter: MultiFrameResultCrossFilter!
    ...
    private func configureCVR() -> Void {
        cvr = CaptureVisionRouter()

        try? cvr.initSettingsFromFile("PassportScanner.json")
        try? cvr.setInput(dce)
        
        // Add filter.
        resultFilter = MultiFrameResultCrossFilter()
        resultFilter.enableResultCrossVerification(.textLine, isEnabled: true)
        cvr.addResultFilter(resultFilter)
    }
}
```

### Implement Result Receiver

Set up result callback in order to receive the parsed passport results after the capturing starts.

```swift
import DynamsoftCodeParser
...
// Add CapturedResultReceiver to the class.
class ViewController: UIViewController, CapturedResultReceiver {
    ...
    private func configureCVR() -> Void {
        ...
        // Add a CaptureResultReceiver to receive results.
        cvr.addResultReceiver(self)
    }
    
    func onParsedResultsReceived(_ result: ParsedResult) {
        // Deal with the parsed results.
    }
}
```

### Extract Parsed Results

```swift
class ViewController: UIViewController, CapturedResultReceiver {
    ...
    func onParsedResultsReceived(_ result: ParsedResult) {
        guard let items = result.items else { return }
        guard let firstItem = items.first else { return }
        let parsedFields = firstItem.parsedFields
        let passportNumber = parsedFields["passportNumber"] ?? ""
        let sex = parsedFields["sex"] ?? ""
        let issuingState = parsedFields["issuingState"] ?? ""
        let nationality = parsedFields["nationality"] ?? ""
        let secondaryIdentifier = parsedFields["secondaryIdentifier"] ?? ""
        let primaryIdentifier = parsedFields["primaryIdentifier"] ?? ""
        let dateOfBirth = parsedFields["dateOfBirth"] ?? ""
        let dateOfExpiry = parsedFields["dateOfExpiry"] ?? ""
        let parsedString = "Name: " + secondaryIdentifier + " " + primaryIdentifier + "\n" + "Gender: " + sex + "\n" + "Issuing State: " + issuingState + "\n" + "Nationality: " + nationality + "\n" + "Date of Birth(YY-MM-DD): " + dateOfBirth + "\n" + "Date of Expiry(YY-MM-DD): " + dateOfExpiry
        print(parsedString)
    }
}
```

### Configure viewWillAppear, viewWillDisappear, viewDidLoad

Time to configure these core functions that will connect everything together. All of the configuration code such as the *configureCVR* and *configureDCE* goes in *viewDidLoad*. While *viewWillAppear* contains the method that will open the camera and start passport scanning.

```swift
class ViewController: UIViewController, CapturedResultReceiver {
    override func viewDidLoad() {
        super.viewDidLoad()
            // Do any additional setup after loading the view.
        self.title = "PassportScanner"
        
        configureDCE()
        configureCVR()
        dce.open()
        print("Open")
        cvr.startCapturing("ReadPassport") {
            isSuccess, error in
            if let error = error {
                print(error.localizedDescription)
            }
        }
    }
        
    override func viewWillAppear(_ animated: Bool) {
        super.viewWillAppear(animated)
        self.navigationController?.navigationBar.tintColor = .white
        self.navigationController?.navigationBar.titleTextAttributes = [
            NSAttributedString.Key.foregroundColor: UIColor.white]
        self.navigationController?.navigationBar.barTintColor = UIColor(red: 59.003 / 255.0, green: 61.9991 / 255.0, blue: 69.0028 / 255.0, alpha: 1)


    }

    override func viewWillDisappear(_ animated: Bool) {
        super.viewWillDisappear(animated)
        dce.close()
    }
}
```

### Build and Run the Project

1. Before deploying the project, select the device that you want to run your app on.
2. Run the project, then your app will be installed on your device.

>Note: View the similar source code from <a href="https://github.com/Dynamsoft/passport-mrz-scanner-mobile/tree/main/ios/PassportMRZScanner" target="_blank">PassportScanner Sample(Swift)</a>
