---
layout: default-layout
title: Getting Started with Barcode Reader
description: This is the user guide of Dynamsoft Capture Vision Cordova edition - Barcode Reader module
keywords: User guide, Barcode Reader, Cordova, Capture Vision, Dynamsoft
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Guide of Dynamsoft Barcode Reader Cordova
---

# Barcode Reader User Guide for Cordova

In this guide, we will explore the Barcode Reader module of the Dynamsoft Capture Vision library for Cordova.

## Table of Contents

- [Barcode Reader User Guide for Cordova](#barcode-reader-user-guide-for-cordova)
  - [Table of Contents](#table-of-contents)
  - [System Requirements](#system-requirements)
    - [Cordova](#cordova)
    - [Android](#android)
    - [iOS](#ios)
  - [Installation](#installation)
  - [Build Your Barcode Scanner App](#build-your-barcode-scanner-app)
    - [Set up Development Environment](#set-up-development-environment)
    - [Initialize the Project](#initialize-the-project)
    - [Include the Library](#include-the-library)
    - [Initialize the Camera Module](#initialize-the-camera-module)
    - [Configure the Barcode Reader Module](#configure-the-barcode-reader-module)
    - [Run the Project](#run-the-project)
      - [Run Android on Windows](#run-android-on-windows)
      - [Run iOS & Android on macOS](#run-ios--android-on-macos)
  - [Customizing the Barcode Reader](#customizing-the-barcode-reader)
    - [Using the Settings Templates](#using-the-settings-templates)
    - [Using the DBRRuntimeSettings Interface](#using-the-dbrruntimesettings-interface)
    - [Customizing the Scan Region](#customizing-the-scan-region)
  - [Licensing](#licensing)

## System Requirements

### Cordova

### Android

### iOS

## Installation

- Install from GitHub

```bash
cordova plugin add https://github.com/Dynamsoft/capture-vision-cordova
```

- Install from npm

```bash
cordova plugin add dynamsoft-capture-vision-cordova
```

## Build Your Barcode Scanner App

Now you will learn how to create a simple barcode scanner using Dynamsoft Capture Vision Cordova SDK.

>Note: Instead of following this guide, you can also initialize a project with this template to get started: <a href="https://github.com/Dynamsoft/capture-vision-cordova-samples/tree/main/BarcodeReaderSimpleSample" target="_blank">Barcode Reader Simple Sample</a>.

### Set up Development Environment

If you are a beginner with Cordova, please follow the guide on the <a href="" target="_blank">Cordova official website</a> to set up the development environment.

### Initialize the Project

Use the following command to create a new project.

```bash
cordova create SimpleBarcodeScanner
```

### Include the Library

```bash
cordova plugin add dynamsoft-capture-vision-cordova
```

### Initialize the Camera Module

Dynamsoft Capture Vision provides a build-in camera module for you to capture and display the video stream. The following two classes are used when initializing the camera module:

- `DCVCameraEnhancer`: The class that provides camera controlling APIs.
- `DCVCameraView`: The class of camera view. The camera view will display the video stream and other UI elements.

1. Find the **www/index.html** file in your project. Replace the original content with the following code:

    ```html
    <!DOCTYPE html>
    <html>
        <body style="margin: 0;">
            <div id="camera_view" style="width: 100vw; height: 100vh; z-index: -1;">
                <div id="show_result" style="position: fixed; width: 100vw; bottom: 10vh;  text-align:center; color: white; "></div>
            </div>
            <script src="cordova.js"></script>
            <script src="js/startup.js"></script>
        </body>
    </html>
    ```

2. Open **www/index.js**, add code to initialize DCVCameraEnhancer and DCVCameraView

    ```js
    // Register the event of device ready.
    document.addEventListener('deviceready', onDeviceReady, false);
    // Create a object of DCVCameraEnhancer.
    var dcvCameraEnhancer
    // Get the camera_view <div> we created in the previous step.
    const cameraViewElement = document.getElementById("camera_view")

    async function onDeviceReady() {
        // Create the instance of DCVCameraEnhancer.
        dcvCameraEnhancer = await Dynamsoft.DCVCameraEnhancer.createInstance()
        // Create the instance of DCVCameraView.
        var cameraView = new Dynamsoft.DCVCameraView()
        // Bind the instance of DCVCameraView with the div you created before.
        cameraView.bindCameraViewToElement(cameraViewElement)
    }
    ```

### Configure the Barcode Reader Module

The Barcode Reader module of DynamsoftCapture Vision needs a valid license to work.

1. Add the following code in **www/index.js** to initialize the license of Barcode Reader module

    ```js
    async function onDeviceReady() {
        ...
        // Here we use a public trial key as an example.
        try {
            await Dynamsoft.DCVBarcodeReader.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9");
        } catch (e) {
            console.log(e)
        }
    }
    ```

2. Initialize the barcode reader module. Register a result listener for obtaining the barcode results.

    ```js
    async function onDeviceReady() {
        ...
        // Create the instance of DCVBarcodeReader.
        dcvBarcodeReader = await Dynamsoft.DCVBarcodeReader.createInstance()
        dcvBarcodeReader.setTextResultListener((results) => {
            const resultElement = document.getElementById('show_result');
            var resultStr = ""
            if (results && results.length > 0) {
                for (i = 0; i < results.length; i++) {
                    resultStr=resultStr + results[i].barcodeFormatString+":"+results[i].barcodeText+'\n'
                }
                resultElement.innerHTML = (resultStr)
            } else {
                resultElement.innerHTML = "No barcode detected in this frame."
            }
            document.querySelector('#camera_view').appendChild(resultElement)
        })
    }
    ```

3. Open the camera and start barcode scanning. You will receive the barcode results from the result listener.

    ```js
    async function onDeviceReady() {
        ...
        dcvCameraEnhancer.open()
        dcvBarcodeReader.startScanning()
    }
    ```

4. Register the event listener of `onResume` and `onPasue` so that the library can stop/restart barcode decoding when the app is pasue/resume.

    ```js
    document.addEventListener('resume', onResume, false);
    document.addEventListener('pause', onPause, false);

    ...

    function onResume() {
        dcvCameraEnhancer.open()
        dcvBarcodeReader.startScanning()
    }

    function onPause() {
        dcvCameraEnhancer.close()
        dcvBarcodeReader.stopScanning()
    }
    ```

### Run the Project

#### Run Android on Windows

Add the platform first.

```bash
cordova platform add android
```

Run the Project.

```bash
cordova run
```

#### Run iOS & Android on macOS

Add the platform first.

```bash
// Add iOS
cordova platform add ios
// Add Android
cordova platform add android
```

Run the Project.

```bash
cordova run
```

## Customizing the Barcode Reader

### Using the Settings Templates

DBR offers several preset templates for different popular scenarios. For example, to prioritize speed over accuracy, you can use one of the speed templates and choose the corresponding template for images or video, and vice versa if you’re looking to prioritize read rate and accuracy over speed. For the full set of templates, please refer to `EnumPresetTemplate`. Here is a quick example of prioritizing read rate for image-based decoding:

```js
```

### Using the DBRRuntimeSettings Interface

The SDK also supports a more granular control over the individual runtime settings rather than using a preset template. The main settings that you can control via this interface are which barcode formats to read, the expected number of barcodes to be read in a single image or frame, and the timeout. For more info on each, please refer to `DBRRuntimeSettings`. Here is a quick example:

```js
```

### Customizing the Scan Region

You can also limit the scan region of the SDK so that it doesn’t exhaust resources trying to read from the entire image or frame. In order to do this, we will need to use the `Region` class as well as the `DCVCameraEnhancer` class.

How to set scan region:

- Define a `Region` object via class Region.
- Configure the value of `Region`.
- Assign the `Region` to the `ScanRegion` property of the `IDCVCameraEnhancer` object.

```js
```

## Licensing

- The `BarcodeReader` module of Dynamsoft Capture Vision needs a valid license to work.
- A one-day trial license is available by default for every new device to try Dynamsoft Capture Vision.
- You can <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=dbr&package=mobile&utm_source=docs" target="_blank"> request a 30-day free trial license</a> via Dynamsoft customer portal for further evaluation.
- [Contact us](https://www.dynamsoft.com/company/contact/) to purchase a full license.