---
layout: default-layout
title: Getting Started with Barcode Reader - Dynamsoft Capture Vision React Native Edition
description: This page is the user guide of Dynamsoft Capture Vision - Barcode Reader module
keywords: User guide, Barcode Reader
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Guide of Barcode Reader
---

# Dynamsoft Capture Vision - Barcode Reader User Guide

In this guide, we will explore the Barcode Reader module of the Dynamsoft Capture Vision library.

<span style="font-size:20px">Table of Contents</span>

* [Getting Started with the Barcode Reader](#getting-started-with-the-barcode-reader)
    * [Initialize the Project](#initialize-the-project)
    * [Include the Barcode Reader Library](#include-the-barcode-reader-library)
    * [Configure the Barcode Reader](#configure-the-barcode-reader)
    * [Rendering the DynamsoftCameraView UI](#rendering-the-dynamsoftcameraview-ui)
  * [Customize the UI](#customize-the-ui-optional)
* [Customizing the Barcode Reader](#customizing-the-barcode-reader)
* [API Documentation](#api-documentation)

## Requirements

### React Native

- Supported Version: 0.60 or higher

### Android

- Supported OS: <a href="https://developer.android.com/about/versions/lollipop" target="_blank">Android 5.0 (API Level 21)</a> or higher.
- Supported ABI: **armeabi-v7a**, **arm64-v8a**, **x86** and **x86_64**.
- Development Environment: Android Studio 3.4+ (Android Studio 4.2+ recommended).

### iOS

- Supported OS: **iOS 10.0** or higher.
- Supported ABI: **arm64** and **x86_64**.
- Development Environment: Xcode 7.1 and above (Xcode 13.0+ recommended).

## Getting Started with the Barcode Reader

### Initialize the Project

Create a new React Native project

    ```bash
    npx react-native init helloBarcodeReader
    ```

### Include the Barcode Reader Library

In the **package.json** of your React Native project, add the following dependencies:

    ```json
    "dependencies": {
        "react": "17.0.2",
        "react-native": "0.65.0",
        "dynamsoft-capture-vision-react-native": "^1.0.0"
    }
    ```

Install the library with NPM or YARN

    ```bash
    npm install
    ```

    Or

    ```bash
    yarn install
    ```

Alternatively, you can include the library by installing it directly via `npm` or `yarn` in the terminal as such

```bash
npm install dynamsoft-capture-vision-react-native@1.0.0

yarn add dynamsoft-capture-vision-react-native@1.0.0
```

### Configure the Barcode Reader

1. In `App.js` include the following libraries:

    ```js
    import React from 'react';
    import {Text} from 'react-native';
    import {
        DynamsoftBarcodeReader,
        DynamsoftCameraView,
        BarcodeResult,
        EnumDBRPresetTemplate,
        EnumBarcodeFormat,
        DBRRuntimeSettings
    } from 'dynamsoft-capture-vision-react-native';
    ```

2. Next in `App.js`, let's define the `state` to your component. In the `state`, add a `results` value, initialized to null. In the following steps, we will store the newly decoded barcodes to `results`.

    ```js
    class App extends React.Component {
        state = {
            results: null
        };
    }
    export default App;
    ```

3. Next is the `componentDidMount` implementation. First up is adding the code to enable barcode decoding:

    ```js
    componentDidMount() {
        (async () => {
            // Initialize the license so that you can use full feature of the Barcode Reader module.
            try {
                await DynamsoftBarcodeReader.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9")
            } catch (e) {
                console.log(e.code);
            }
            // Create a barcode reader instance.
            this.reader = await DynamsoftBarcodeReader.createInstance();
            // Enable video barcode scanning.
            // If the camera is opened, the barcode reader will start the barcode decoding thread when you triggered the startScanning.
            // The barcode reader will scan the barcodes continuously before you trigger stopScanning.
            await this.reader.startScanning();
            // Add a result listener. The result listener will handle callback when barcode result is returned. 
            this.reader.addResultListener((results: BarcodeResult[]) => {
                // Update the newly detected barcode results to the state.
                this.setState({results: results});
            });
        })();
    }
    ```

4. After implementing `componentDidMount`, `componentWillUnmount` will then include code to stop the barcode decoding thread and remove the result listener.

    ```js
    async componentWillUnmount() {
        // Stop the barcode decoding thread when your component is unmount.
        await this.reader.stopScanning();
        // Remove the result listener when your component is unmount.
        this.reader.removeAllResultListeners();
    }
    ```

### Rendering the DynamsoftCameraView UI

Lastly, let's create the `DynamsoftCameraView` UI componment in the `render` function.

    ```js
    render() {
        // Add code to fetch barcode text and format from the BarcodeResult
        let results: BarcodeResult[] = this.state.results;
        let resultBoxText: String = "";
        if (results && results.length>0){
            for (let i=0;i<results.length;i++){
                resultBoxText+=results[i].barcodeFormatString+"\n"+results[i].barcodeText+"\n";
            }
        }
        // Render DynamsoftCameraView componment.
        return (
            <DynamsoftCameraView
                style={{
                    flex: 1,
                }}
                ref = {(ref)=>{this.scanner = ref}}
                isOverlayVisible={true}
            >
    // Add a text box to display the barcode result.
                <Text style={{
                    flex: 0.9,
                    textAlignVertical: "bottom",
                    textAlign: "center",
                    color: "white",
                    fontSize: 18,
                }}>{results && results.length > 0 ? resultBoxText : "No Barcode Detected"}</Text>
            </DynamsoftCameraView>
        );
    }
    ```

### Configure Camera Permissions

You need to set the "Privacy - Camera Usage Description" field in the Info.plist file for iOS.

## Customizing the Barcode Reader

There are several ways in which you can customize the Barcode Reader - but what they all have in common is that each involves the [`updateRuntimeSettings`](../api-reference/barcode-reader.md#updateruntimesettings) method. There are currently three methods in which you can update the runtime settings.

### Run the Project

#### Run Android on Windows

In the command lines, go to your project folder and run the following command:

```bash
npx react-native run-android
```

#### Run iOS on macOS

In the command lines, go to the iOS folder in your project:

```bash
cd ios
```

Use pod install to include the libraries:

```bash
pod install
```

Go back to the project folder and run the project:

```bash
cd ..
```

```bash
npx react-native run-ios
```
