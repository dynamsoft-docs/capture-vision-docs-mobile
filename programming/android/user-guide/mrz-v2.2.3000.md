---
layout: default-layout
title: Scan & Parse MRZ - Dynamsoft Capture Vision Android Edition
description: This page introduce how to scan and parse a MRZ with Dynamsoft Capture Vision Android Edition.
keywords: Android, MRZ, passport, id card, visa
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Android User Guide for MRZ Integration

In this guide, you will learn step by step on how to build a MRZ scanner application with Dynamsoft Capture Vision Android SDK.

- [Android User Guide for MRZ Integration](#android-user-guide-for-mrz-integration)
	- [Supported Machine-Readable Travel Document Types](#supported-machine-readable-travel-document-types)
		- [ID (TD1 Size)](#id-td1-size)
		- [ID (TD2 Size)](#id-td2-size)
		- [Passport (TD3 Size)](#passport-td3-size)
	- [Requirements](#requirements)
	- [Add the SDK](#add-the-sdk)
	- [Build Your First Application](#build-your-first-application)
		- [Create a New Project](#create-a-new-project)
		- [Include the Libraries](#include-the-libraries)
		- [Deploy the CharacterModel \& Template](#deploy-the-charactermodel--template)
		- [Initialize License](#initialize-license)
		- [Initialize the Camera Module](#initialize-the-camera-module)
		- [Initialize Capture Vision Router](#initialize-capture-vision-router)
		- [Extract Parsed Results](#extract-parsed-results)
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

- Supported OS: Android 5.0 (API Level 21) or higher.
- Supported ABI: **armeabi-v7a**, **arm64-v8a**, **x86** and **x86_64**.
- Development Environment: Android Studio 2022.2.1 or higher.

## Add the SDK

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
        implementation 'com.dynamsoft:dynamsoftcapturevisionbundle:2.2.3000'
    }
    ```

    > Read more about the modules of [dynamsoftcapturevisionbundle](../api-reference/index.md)

3. Click **Sync Now**. After the synchronization is complete, the SDK is added to the project.

## Build Your First Application

In this section, we will explain how to create a `HelloWorld` implementation similar to our simple `MRZScanner` app for reading the MRZ zone from camera video input.

>Note:
>
>- Android Studio 2024.1.1 is used here in this guide.
>- You can get similar source code from
>    - <a href="https://github.com/Dynamsoft/mrz-scanner-mobile/tree/main/android/MRZScanner/" target="_blank">MRZScanner Sample(Java)</a>

### Create a New Project

1. Open Android Studio, select **File > New > New Project**.

2. Choose the correct template for your project. In this sample, we use **Empty Views Activity**.

3. When prompted, set your app name to  `HelloWorld` and set the **Save** location, **Language**, and **Minimum SDK** (we use 21 here).
    > Note:
    >
    > - With **minSdkVersion** set to 21, your app is compatible with more than 99.6% of devices on the Google Play Store (last update: October 2023).

### Include the Libraries

Add the SDK to your new project. Please read [Add the SDK](#add-the-sdk) section for more details.

### Deploy the CharacterModel & Template

A `CharacterModel` is a model file trained using deep neural networks for character recognition. A `Template` file in the Dynamsoft Capture Vision SDK offers a customizable configuration for optimizing barcode recognition, label recognition, document normalization, and bytes parsing settings. This enables users to tailor the capture process to their specific needs. For MRZ scanning, you have to include the required the MRZ `CharacterModel` and `Template` in your project first.

1. Right-click on the **app** folder, click **New->Directory** and select the **src\main\assets** to create an assets folder. Under the **assets** folder create two new folders, **CharacterModel** and **Templates**.

2. Copy the <a href="https://cdn.jsdelivr.net/npm/dynamsoft-label-recognizer-data@1.0.11/dist/MRZ.data" target="_blank">**MRZ.data**</a> to the **CharacterModel** folder.

3. Copy the  <a href="https://github.com/Dynamsoft/mrz-scanner-mobile/blob/main/android/MRZScanner/app/src/main/assets/Templates/MRZScanner.json" target="_blank">**MRZScanner.json**</a> to the **Templates** folder.

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
                   error.printStackTrace();
               });
           }
       }
   }
   ```

   >Note:  
   >
   >- The license string here grants a time-limited free trial which requires network connection to work.
   >- You can request for a 30-day trial license via the <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=mrz&utm_source=docs&package=android" target="_blank">Trial License link</a>.

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

2. Create a `CapturedResultReceiver` and register with the `CaptureVisionRouter` instance to get the result of MRZ parsing.

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

3. Initialize settings via a MRZ scanning template.

    ````java
    try {
        mRouter.initSettingsFromFile("MRZScanner.json");
    } catch (CaptureVisionRouterException e) {
        throw new RuntimeException(e);
    }
    ```

4. Override `MainActivity.onResume` and `MainActivity.onPause` functions to start/stop video MRZ scanning. After scanning starts, the SDK will automatically recognize and parse the text in the MRZ area from the video frame, and send the parsed MRZ result to the callback function.

    ```java
    import com.dynamsoft.dce.CameraEnhancerException;
    public class MainActivity extends AppCompatActivity {
        ...
        @Override
        public void onResume() {
            super.onResume();
            // Start video MRZ reading
            try {
                mCamera.open();
            } catch (CameraEnhancerException e) {
                e.printStackTrace();
            }
            mRouter.startCapturing("ReadPassportAndId", new CompletionListener() {
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
            // Stop video MRZ reading
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
    String number = entry.get("passportNumber") == null ? entry.get("documentNumber") : entry.get("passportNumber");
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

- <a href="https://github.com/Dynamsoft/mrz-scanner-mobile/tree/main/android/MRZScanner/" target="_blank">MRZScanner Sample(Java)</a>
