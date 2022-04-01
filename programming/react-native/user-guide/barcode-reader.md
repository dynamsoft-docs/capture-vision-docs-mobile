---
layout: default-layout
title: Getting Started with Barcode Reader
description: This page is the user guide of Dynamsoft Capture Vision - Barcode Reader module
keywords: User guide, Barcode Reader
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Guide of Barcode Reader
---

# Getting Started with Barcode Reader

## Add Configurations for Barcode Decoding

1. In `App.js` include the following libaries:

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

2. Add `state` to your component. In the state, add a `results` value. In the following steps, we will store the newly decoded barcodes to the `results`.

```js
class App extends React.Component {
    state = {
        results: null
    };
}
export default App;
```

3. In `componentDidMount`, add the following code to enable barcode decoding.

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

4. In `componentWillUnmount`, add code to stop the barcode decoding thread and remove the result listener.

```js
async componentWillUnmount() {
    // Stop the barcode decoding thread when your component is unmount.
    await this.reader.stopScanning();
    // Remove the result listener when your component is unmount.
    this.reader.removeAllResultListener();
}
```

5. Render the `DynamsoftCameraView` componment.

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
