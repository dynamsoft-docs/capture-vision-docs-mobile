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

* [System Requirements](#system-requirements)
* [Getting Started with the Barcode Reader](#getting-started-with-the-barcode-reader)
    * [Initialize the Project](#initialize-the-project)
    * [Include the Barcode Reader Library](#include-the-barcode-reader-library)
    * [Configure the Barcode Reader](#configure-the-barcode-reader)
    * [Rendering the UI](#rendering-the-ui)
* [Customizing the Barcode Reader](#customizing-the-barcode-reader)
    * [Using the settings templates](#using-the-settings-templates)
    * [Using the DBRRuntimeSettings interface](#using-the-dbrruntimesettings-interface)
    * [Customizing the scan region](#customizing-the-scan-region)
* [Run the Project](#run-the-project)

## System Requirements

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

> Alternatively, you can include the library by installing it directly via `npm` or `yarn` in the terminal as such
> 
> ```bash
> npm install dynamsoft-capture-vision-react-native@1.0.0
> 
> yarn add dynamsoft-capture-vision-react-native@1.0.0
> ```

**For iOS**: In the terminal, go to the `ios` folder in your project:

```bash
cd ios
```

Then, use `pod install` to include the cocoapods libraries necessary to run the app on iOS:

```bash
pod install
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

### Rendering the UI

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

You need to set the "Privacy - Camera Usage Description" field in the Info.plist file for iOS. If this property is not set, the iOS application will fail at runtime. In order to set this property, you might need to use Xcode and open the corresponding xcworkspace located in the `ios` folder.

## Customizing the Barcode Reader

There are several ways in which you can customize the Barcode Reader - but what they all have in common is that each involves the [`updateRuntimeSettings`](../api-reference/barcode-reader.md#updateruntimesettings) method. There are currently three methods in which you can update the runtime settings.

### Using the settings templates

DBR offers a number of preset templates for different popular scenarios. To prioritize speed over accuracy, then you will want to use one of the speed templates, choosing the corresponding template for images or video, respectively. And vice versa if you're looking to prioritize read rate and accuracy over speed. For the full set of templates, please refer to [`EnumPresetTemplate`](../api-reference/enum-dbr-preset-template.md). Here is a quick example:

`await this.reader.updateDBRRuntimeSettings(EnumDBRPresetTemplate.VIDEO_SPEED_FIRST);`

### Using the DBRRuntimeSettings interface

The SDK also supports a more granular control over the individual runtime settings rather than using a preset template. The main settings that you can control via this interface are which barcode formats to read, the expected number of barcodes to be read in a single image or frame, and the timout. For more info on each, please refer to [`DBRRuntimeSettings`](../api-reference/interface-dbr-runtime-settings.md). Here is a quick exmaple:

```js
let settings: DBRRuntimeSettings = await this.reader.getDBRRuntimeSettings();
// Set the expected barcode count to 0 when you are not sure how many barcodes you are scanning.
// Set the expected barcode count to 1 can maximize the barcode decoding speed.
settings.expectedBarcodesCount = 0;
settings.barcodeFormatIds = EnumBarcodeFormat.BF_ONED | EnumBarcodeFormat.BF_QR_CODE;
await this.reader.updateDBRRuntimeSettings(settings)
```

### Customizing the scan region

You can also limit the scan region of the SDK so that it doesn't exhaust resources trying to read from the entire image or frame. In order to do this, we will need to use the [`Region`](../api-reference/interface-region.md) interface as well as the [`DynamsoftCameraView`](../api-reference/camera-view.md) component.

First, the region must be defined using the Region interface. In this example, we demonstrate how the region is first defined in the `render()` function and then assigned to the `scanRegion` parameter of the `DynamsoftCameraView` component:

```js
let region: Region;        
let barcode_text = "";
region = {
    regionTop: 30,
    regionLeft: 15,
    regionBottom: 70,
    regionRight: 85,
    regionMeasuredByPercentage: true
}
...
        <DynamsoftCameraView
            style={{
                flex: 1,
            }}
            ref = {(ref)=>{this.scanner = ref}}
            overlayVisible={true}
            scanRegionVisible={true}
            scanRegion={region}
        >
```

## Run the Project

### Run Android on Windows

In the command line interface (we recommend using Powershell), go to your project folder and run the following command:

```bash
npx react-native run-android
```

### Run iOS on macOS

In the terminal, go to the project folder in your project:

```bash
npx react-native run-ios
```

> Note: The application needs to run on a physical device rather than a simulator as it requires the use of the camera. If you try running it on a simulator, you will most likely run into a number of errors/failures. 
> On iOS, in order to run the React Native app on a physical device you will need to install the [`ios-deploy`](https://www.npmjs.com/package/ios-deploy) library. Afterwards, you can run the react native app from the terminal as such `npx react-native run-ios --device` assuming it's the only device connected to the Mac.
> Alternatively on iOS, you can simply open the xcworkspace of the project found in the `ios` folder using Xcode and run the sample on your connected iOS device from there. The advantage that this offers is that it is easier to deal with the developer signatures for deployment in there.
