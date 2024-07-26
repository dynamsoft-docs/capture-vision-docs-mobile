---
layout: default-layout
title: Scan & Parse Passport - Dynamsoft Capture Vision Android Edition
description: This page introduce how to scan and parse a passport with Dynamsoft Capture Vision Android Edition.
keywords: Android, passport
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# Android User Guide for Passport Integration

## Requirements

- Supported OS: Android 5.0 (API Level 21) or higher.
- Supported ABI: **armeabi-v7a**, **arm64-v8a**, **x86** and **x86_64**.
- Development Environment: Android Studio 2022.2.1 or higher.

## Add the Libraries

To build the passport application, it is essential to integrate the following libraries from the Dynamsoft Capture Vision SDK:

   | File | Description |
   |---------|-------------|
   | `DynamsoftCaptureVisionRouter.aar` | The Dynamsoft Capture Vision Router module is the cornerstone of the Dynamsoft Capture Vision (DCV) architecture. It focuses on coordinating batch image processing and provides APIs for setting up image sources and result receivers, configuring workflows with parameters, and controlling processes. |
   | `DynamsoftLabelRecognizer.aar` | The Dynamsoft Label Recognizer module identifies and recognizes text labels such as passport MRZs, ID cards, and VIN numbers. |
   | `DynamsoftCore.aar` | The Dynamsoft Core module lays the foundation for Dynamsoft SDKs based on the DCV (Dynamsoft Capture Vision) architecture. It encapsulates the basic classes, interfaces, and enumerations shared by these SDKs.|
   | `DynamsoftImageProcessing.aar` | The Dynamsoft Image Processing module facilitates digital image processing and supports operations for other modules, including the Barcode Reader, Label Recognizer, and Document Normalizer.  |
   | `DynamsoftNeuralNetwork.aar` | The Dynamsoft Neural Network module allows SDKs compliant with the DCV (Dynamsoft Capture Vision) architecture to leverage the power of deep learning when processing digital images. |
   | `DynamsoftLicense.aar` | The Dynamsoft License module manages the licensing aspects of Dynamsoft SDKs based on the DCV (Dynamsoft Capture Vision) architecture. |
   | `DynamsoftCameraEnhancer.aar` | The <a href="/camera-enhancer/docs/mobile/programming/android/" target="_blank">Dynamsoft Camera Enhancer (DCE) module</a> controls the camera, transforming it into an image source for the DCV (Dynamsoft Capture Vision) architecture through ISA implementation. It also enhances image quality during acquisition and provides basic viewers for user interaction. |
   | `DynamsoftUtility.aar` | The Dynamsoft Utility module defines auxiliary classes, including the ImageManager, and implementations of the CRF (Captured Result Filter) and ISA (Image Source Adapter). These are shared by all Dynamsoft SDKs based on the DCV (Dynamsoft Capture Vision) architecture. |
   | `DynamsoftCodeParser.aar` | The Dynamsoft Code Parser module converts data strings, typically encrypted in barcodes and machine-readable zones, into human-readable information. |
   | `DynamsoftCodeParserDedicator.aar` | The Dynamsoft Code Parser Dedicator module provides auxiliary functionality to enhance and extend the capabilities of DCP module. |

1. Open the file `[App Project Root Path]\app\build.gradle` and add the Maven repository:

    ```groovy
    allprojects {
        repositories {
            maven {
                url "https://download2.dynamsoft.com/maven/aar"
            }
        }
    }
    ```

2. Add the references in the dependencies:

    ```groovy
    dependencies {
        implementation 'com.dynamsoft:dynamsoftlabelrecognizerbundle:3.2.3000'
        implementation 'com.dynamsoft:dynamsoftcodeparser:2.2.11'
        implementation 'com.dynamsoft:dynamsoftcodeparserdedicator:1.2.20'
    }
    ```

3. Click **Sync Now**. After the synchronization is complete, the SDK is added to the project.

## Build Your First Application

In this section, we will explain how to create a `HelloWorld` implementation similar to our simple `PassportMRZScanner` app for reading the MRZ zone from camera video input.

>Note:
>
>- Android Studio 2022.3.1 is used here in this guide.
>- You can get similar source code from
>    - <a href="https://github.com/Dynamsoft/passport-mrz-scanner-mobile/tree/main/android/PassportMRZScanner/" target="_blank">PassportMRZScanner Sample(Java)</a>

### Create a New Project

1. Open Android Studio, select **File > New > New Project**.

2. Choose the correct template for your project. In this sample, we use **Empty Views Activity**.

3. When prompted, set your app name to  `HelloWorld` and set the **Save** location, **Language**, and **Minimum SDK** (we use 21 here).
    > Note:
    >
    > - With **minSdkVersion** set to 21, your app is compatible with more than 99.6% of devices on the Google Play Store (last update: October 2023).

### Include the Libraries

Add the SDK to your new project. Please read [Add the Libraries](#add-the-libraries) section for more details.

### Deploy the CharacterModel & Template

A `CharacterModel` is a model file trained using deep neural networks for character recognition. A `Template` file in the Dynamsoft Capture Vision SDK offers a customizable configuration for optimizing barcode recognition, label recognition, document normalization, and bytes parsing settings. This enables users to tailor the capture process to their specific needs. For passport scanning, you have to include the required the MRZ `CharacterModel` and `Template` in your project first.

1. Right-click on the **app** folder, click **New->Directory** and select the **src\main\assets** to create an assets folder. Under the **assets** folder create two new folders, **CharacterModel** and **Templates**.

2. Copy the <a href="https://cdn.jsdelivr.net/npm/dynamsoft-label-recognizer-data@1.0.11/dist/MRZ.data" target="_blank">**MRZ.data**</a> to the **CharacterModel** folder.

3. Copy the  <a href="https://github.com/Dynamsoft/passport-mrz-scanner-mobile/blob/main/android/PassportMRZScanner/app/src/main/assets/Templates/PassportScanner.json" target="_blank">**PassportMRZScanner.json**</a> to the **Templates** folder.

### Initialize License

1. Initialize the license in the file `MainActivity.java`.

   ```java
   import com.dynamsoft.license.LicenseManager;
   public class MainActivity extends AppCompatActivity {
      @Override
      protected void onCreate(Bundle savedInstanceState) {
             super.onCreate(savedInstanceState);
             setContentView(R.layout.activity_main);
             if (savedInstanceState == null) {
                LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", this, (isSuccess, error) -> {
                   if (!isSuccess) {
                      error.printStackTrace();
                   }
                });
             }
      }
   }
   ```

   >Note:  
   >
   >- The license string here grants a time-limited free trial which requires network connection to work.
   >- You can request for a 30-day trial license via the <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=passport&utm_source=docs&package=android" target="_blank">Trial License link</a>. Offline trial license is also available by <a href="https://www.dynamsoft.com/contact/" target="_blank">contacting us</a>.

### Initialize the Camera Module

1. In the Project window, open **app > res > layout > `activity_main.xml`** and create a DCE camera view section under the root node.

   ```xml
    <com.dynamsoft.dce.CameraView
        android:id="@+id/camera_view"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
    ```

2. Import the Dynamsoft Camera Enhancer module, initialize the camera view, and bind to the created `CameraEnhancer` instance in the  `MainActivity.java` file.

   ```java
   import com.dynamsoft.dce.CameraView;
   import com.dynamsoft.dce.CameraEnhancer;
   import com.dynamsoft.dce.utils.PermissionUtil;
   public class MainActivity extends AppCompatActivity {
      CameraEnhancer mCamera;
      @Override
      protected void onCreate(Bundle savedInstanceState) {
             ...
             // Add camera view for previewing video.
             PermissionUtil.requestCameraPermission(this);
             CameraView cameraView = findViewById(R.id.camera_view);
             mCamera = new CameraEnhancer(cameraView, this);
      }
   }
   ```

### Initialize Capture Vision Router

1. Import and initialize the `CaptureVisionRouter` and set the previously created `CameraEnhancer` instance as its input.

   ```java
   import com.dynamsoft.cvr.CaptureVisionRouter;
   import com.dynamsoft.cvr.CaptureVisionRouterException;
   public class MainActivity extends AppCompatActivity {
      ...
      private CaptureVisionRouter mRouter;
      @Override
      protected void onCreate(Bundle savedInstanceState) {
             ...
             mRouter = new CaptureVisionRouter(this);
             try {
                mRouter.setInput(mCamera);
             } catch (CaptureVisionRouterException e) {
                throw new RuntimeException(e);
             }
      }
   }
   ```

2. Create a `CapturedResultReceiver` and register with the `CaptureVisionRouter` instance to get the result of passport parsing.

    ```java
    import com.dynamsoft.core.basic_structures.CapturedResultReceiver;
    import com.dynamsoft.dlr.RecognizedTextLinesResult;
    import com.dynamsoft.dcp.ParsedResult;
    ...
    public class MainActivity extends AppCompatActivity {
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            ...
            mRouter.addResultReceiver(new CapturedResultReceiver() {
                @Override
                public void onParsedResultsReceived(@NonNull ParsedResult result)
                {
                }
            });
        }
    }
    ```

3. Initialize settings via a passport scanning template.

    ````java
    try {
        mRouter.initSettingsFromFile("PassportMRZScanner.json");
    } catch (CaptureVisionRouterException e) {
        throw new RuntimeException(e);
    }
    ```

4. Override `MainActivity.onResume` and `MainActivity.onPause` functions to start/stop video passport scanning. After scanning starts, the SDK will automatically recognize and parse the text in the MRZ area from the video frame, and send the parsed passport result to the callback function.

    ```java
    import com.dynamsoft.dce.CameraEnhancerException;
    public class MainActivity extends AppCompatActivity {
        ...
        @Override
        public void onResume() {
            super.onResume();
            // Start video passport reading
            try {
                mCamera.open();
            } catch (CameraEnhancerException e) {
                e.printStackTrace();
            }
            mRouter.startCapturing("ReadPassport", new CompletionListener() {
                @Override
                public void onSuccess() {}
                @Override
                public void onFailure(int errorCode, String errorString) {
                    runOnUiThread(() -> showDialog("Error", String.format(Locale.getDefault(), "ErrorCode: %d %nErrorMessage: %s", errorCode, errorString)));
                }
            });
        }
        @Override
        public void onPause() {
            super.onPause();
            // Stop video passport reading
            try {
                mCamera.close();
            } catch (CameraEnhancerException e) {
                e.printStackTrace();
            }
            mRouter.stopCapturing();
        }
    }
    ```

### Extract Parsed Results

```java
import com.dynamsoft.dcp.ParsedResultItem;
...
@Override
public void onParsedResultsReceived(@NonNull ParsedResult result) {
    if (!succeed) {
        onParsedResultReceived(result);
    }
}
...
private void onParsedResultReceived(ParsedResult result) {
    if (result.getItems() == null) {
        return;
    }
    // ParsedResult contains an array of ParsedResultItem, which stores the parse fields and values.
    // If the library failed to parse the content, the array length will be 0.
    if (result.getItems().length == 0) {
        // Do something when the library fails to parse the content.
    } else {
        // The assembleString method is implemented below. It gets all parse fields and assemble them into a string.
        String labelText = assembleString(result.getItems()[0]);
        if (labelText != null) {
            // Do something to display the result.
        }else {
            // Do something when the library fails to parse the content.
        }
    }
}
// This method is an example for how to extract the parsed information from a ParsedResultItem.
private String assembleString(ParsedResultItem item) {
    HashMap<String, String> entry = item.getParsedFields();
    String number = entry.get("passportNumber");
    mName = entry.get("secondaryIdentifier") + " " + entry.get("primaryIdentifier");
    if (number == null ||
            entry.get("sex") == null ||
            entry.get("issuingState") == null ||
            entry.get("nationality") == null ||
            entry.get("secondaryIdentifier") == null ||
            entry.get("primaryIdentifier") == null ||
            entry.get("dateOfBirth") == null ||
            entry.get("dateOfExpiry") == null) {
        return null;
    }
    return "Document Type: " + item.getCodeType() + "\n" +
            "Document Number: " + number + "\n" +
            "Surname: " + entry.get("primaryIdentifier") + "\n" +
            "Given name: " + entry.get("secondaryIdentifier") + "\n" +
            "Gender: " + entry.get("sex") + "\n" +
            "Issuing State: " + entry.get("issuingState") + "\n" +
            "Nationality: " + entry.get("nationality") + "\n" +
            "Date of Birth(YY-MM-DD): " + entry.get("dateOfBirth") + "\n" +
            "Date of Expiry(YY-MM-DD): " + entry.get("dateOfExpiry") + "\n";
}
```

### Build and Run the Project

1. Select the device that you want to run your app on from the target device drop-down menu in the toolbar.

2. Click the **Run app** button, then Android Studio installs your app on the connected device and launches it.

You can also download the similar source code of all the steps above:

- <a href="https://github.com/Dynamsoft/passport-mrz-scanner-mobile/tree/main/android/PassportMRZScanner/" target="_blank">PassportMRZScanner Sample(Java)</a>
