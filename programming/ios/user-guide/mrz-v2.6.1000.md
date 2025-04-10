---
layout: default-layout
title: Scan & Parse MRZ - Dynamsoft Capture Vision iOS Edition
description: This page introduce how to scan and parse a MRZ with Dynamsoft Capture Vision iOS Edition.
keywords: iOS, MRZ, passport, id card, visa
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# iOS User Guide for MRZ Integration

In this guide, you will learn step by step on how to build a MRZ scanner application with Dynamsoft Capture Vision iOS SDK.

- [iOS User Guide for MRZ Integration](#ios-user-guide-for-mrz-integration)
  - [Supported Machine-Readable Travel Document Types](#supported-machine-readable-travel-document-types)
    - [ID (TD1 Size)](#id-td1-size)
    - [ID (TD2 Size)](#id-td2-size)
    - [Passport (TD3 Size)](#passport-td3-size)
  - [Requirements](#requirements)
  - [Add the SDK](#add-the-sdk)
    - [Add the xcframeworks via CocoaPods](#add-the-xcframeworks-via-cocoapods)
    - [Add the xcframeworks via Swift Package Manager](#add-the-xcframeworks-via-swift-package-manager)
  - [Build Your First Application](#build-your-first-application)
    - [Create a New Project](#create-a-new-project)
    - [Include the Library](#include-the-library)
    - [Initialize the License](#initialize-the-license)
    - [Initialize the Camera Module](#initialize-the-camera-module)
    - [Initialize the Capture Vision Router](#initialize-the-capture-vision-router)
    - [Implement Result Receiver](#implement-result-receiver)
    - [Extract Parsed Results](#extract-parsed-results)
    - [Configure viewWillAppear, viewWillDisappear, viewDidLoad](#configure-viewwillappear-viewwilldisappear-viewdidload)
    - [Configure Camera Privacy](#configure-camera-privacy)
    - [Build and Run the Project](#build-and-run-the-project)

## Supported Machine-Readable Travel Document Types

The Machine Readable Travel Documents (MRTD) standard specified by the International Civil Aviation Organization (ICAO) defines how to encode information for optical character recognition on official travel documents.

Currently, the SDK supports three types of MRTD:

> Note: If you need support for other types of MRTDs, our SDK can be easily customized. Please contact support@dynamsoft.com.

### ID (TD1 Size)

The MRZ (Machine Readable Zone) in TD1 format consists of 3 lines, each containing 30 characters.

<div>
   <img src="{{ site.dcvb_root }}programming/assets/td1-id.png" alt="Example of MRZ in TD1 format" width="60%" />
</div>

### ID (TD2 Size)

The MRZ (Machine Readable Zone) in TD2 format  consists of 2 lines, with each line containing 36 characters.

<div>
   <img src="{{ site.dcvb_root }}programming/assets/td2-id.png" alt="Example of MRZ in TD2 format" width="72%" />
</div>

### Passport (TD3 Size)

The MRZ (Machine Readable Zone) in TD3 format consists of 2 lines, with each line containing 44 characters.

<div>
   <img src="{{ site.dcvb_root }}programming/assets/td3-passport.png" alt="Example of MRZ in TD2 format" width="88%" />
</div>

## Requirements

- Supported OS: iOS 11+ (iOS 13+ recommended).
- Supported ABI: arm64 and x86_64.
- Development Environment: Xcode 13+ (Xcode 14.1+ recommended).

## Add the SDK

There are two ways to add the SDK into your project - **CocoaPods**, or via **Swift Package Manager**.

### Add the xcframeworks via CocoaPods

1. Add the frameworks in your **Podfile**, replace *TargetName* with your real target name.

    ```pod
    target '{Your project name}' do
        use_frameworks!

        pod 'DynamsoftCaptureVisionBundle','2.6.1000'
        pod 'DynamsoftMRZ', '3.4.20'

    end
    ```

    > Read more about the modules of [DynamsoftCaptureVisionBundle](../api-reference/index.md)

2. Execute the pod command to install the frameworks and generate workspace(**{Your project name}.xcworkspace**):

   ```bash
   pod install
   ```

### Add the xcframeworks via Swift Package Manager

1. In your Xcode project, go to **File --> AddPackages**.

2. In the top-right section of the window, search "https://github.com/Dynamsoft/capture-vision-spm"

3. Select `capture-vision-spm`, choose `Exact version`, enter **2.4.2000**, then click **Add Package**.

4. Check all the frameworks and add.

## Build Your First Application

In this section, we will explain how to create a `HelloWorld` implementation similar to our simple `MRZScanner` app for reading the MRZ zone from camera video input.

>Note:
>
>- The following steps are completed in XCode 14.2
>- You can get similar source code from <a href="https://github.com/Dynamsoft/mrz-scanner-mobile/tree/v1.0.0/ios/MRZScanner/" target="_blank">MRZScanner Sample(Swift)</a>

### Create a New Project

1. Open XCode and select *Create a new Xcode Project* or in the *File > New > Project* menu to create a new project.

2. Select **iOS -> App** for your application.

3. Input your product name (HelloWorld), interface (StoryBoard) and language (Swift)

4. Click on **Next** and select the location to save the project.

5. Click on **Create** to finish  creating the new project.

### Include the Library

To add the SDK to your new project, please read [Add the SDK](#add-the-sdk) section for more details.

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
   >- You can request for a 30-day trial license via the <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=mrz&utm_source=docs&package=ios" target="_blank">Trial License link</a>.

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
import DynamsoftUtility
...
class ViewController: UIViewController {
    private var cvr: CaptureVisionRouter!
    private var resultFilter: MultiFrameResultCrossFilter!
    ...
    private func configureCVR() -> Void {
        cvr = CaptureVisionRouter()

        try? cvr.setInput(dce)
        
        // Add filter.
        resultFilter = MultiFrameResultCrossFilter()
        resultFilter.enableResultCrossVerification(.textLine, isEnabled: true)
        cvr.addResultFilter(resultFilter)
    }
}
```

### Implement Result Receiver

Set up result callback in order to receive the parsed MRZ results after the capturing starts.

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
        let passportNumber = parsedFields["passportNumber"] ?? parsedFields["documentNumber"] ?? ""
        let sex = parsedFields["sex"] ?? ""
        let issuingState = parsedFields["issuingState"] ?? ""
        let nationality = firstItem.getFieldRawValue("nationality")
        let secondaryIdentifier = parsedFields["secondaryIdentifier"] ?? ""
        let primaryIdentifier = parsedFields["primaryIdentifier"] ?? ""
        let dateOfBirth = parsedFields["dateOfBirth"] ?? ""
        let dateOfExpiry = parsedFields["dateOfExpiry"] ?? ""
        let parsedString = "Name: " + secondaryIdentifier + " " + primaryIdentifier + "\n" + "Gender: " + sex + "\n" + "Issuing State: " + issuingState + "\n" + "Nationality: " + nationality + "\n" + "Date of Birth(YY-MM-DD): " + dateOfBirth + "\n" + "Date of Expiry(YY-MM-DD): " + dateOfExpiry
    }
}
```

### Configure viewWillAppear, viewWillDisappear, viewDidLoad

Time to configure these core functions that will connect everything together. All of the configuration code such as the *configureCVR* and *configureDCE* goes in *viewDidLoad*. While *viewWillAppear* contains the method that will open the camera and start MRZ scanning.

```swift
class ViewController: UIViewController, CapturedResultReceiver {
    override func viewDidLoad() {
        super.viewDidLoad()
            // Do any additional setup after loading the view.
        self.title = "MRZScanner"
        
        configureDCE()
        configureCVR()
        dce.open()
        print("Open")
        cvr.startCapturing("ReadPassportAndId") {
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

>Note:
>
>- When using `startCapturing`, set the template to "ReadPassportAndId" to capture both Passports and ID cards.
>- If you only need to capture Passports, set the template to "ReadPassport" when calling `startCapturing`.
>- To capture only ID cards, set the template to "ReadId" during `startCapturing`.

### Configure Camera Privacy

Add Privacy - Camera Usage Description to the info.plist of your project to request camera permission. An easy way to do this is to access your project settings, go to Info and then add this Privacy property to the iOS target properties list.

### Build and Run the Project

1. Before deploying the project, select the device that you want to run your app on.
2. Run the project, then your app will be installed on your device.

>Note: View the similar source code from <a href="https://github.com/Dynamsoft/mrz-scanner-mobile/tree/v1.0.0/ios/MRZScanner/" target="_blank">MRZScanner Sample(Swift)</a>
