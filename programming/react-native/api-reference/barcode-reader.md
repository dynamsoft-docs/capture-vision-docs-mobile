---
layout: default-layout
title: Barcode Reader Class of React-Native Dynamsoft Capture Vision
description: This page is the API reference of Barcode Reader class
keywords: Barcode, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Barcode Reader class
---

# DynamsoftBarcodeReader Class

| Methods | Description |
| ------- | ----------- |
| [`initLicense`](#initlicense) | Initialize the license of Dynamsoft Capture Vision.
 |
| [`createInstance`](#createinstance) | Create a barcode reader instance. |
| [`getVersion`](#getversion) | Get the version of `DynamsoftBarcodeReader`, which is packaged in Dynamsoft Capture Vision. |
| [`getDBRRuntimeSettings`](#getdbrruntimesettings) | Get the current runtime settings of `DynamsoftBarcodeReader`. |
| [`updateDBRRuntimeSettings`](#updatedbrruntimesettings) | Update the runtime settings of `DynamsoftBarcodeReader` with a DBRRuntimeSettings struct or a template. |
| [`resetDBRRuntimeSettings`](#resetdbrruntimesettings) | Reset the runtime settings of `DynamsoftBarcodeReader` to default. |
| [`outputDBRRuntimeSettings`](#outputdbrruntimesettings) | Output the runtime settings of `DynamsoftBarcodeReader` to string. |
| [`startBarcodeScanning`](#startbarcodescanning) | Start the barcode decoding thread. |
| [`stopBarcodeScanning`](#stopbarcodescanning) | Stop the barcode decoding thread. |
| [`addFrameListener`](#addframelistener) | Specifies an event handler that fires after the library finishes scanning a frame. |

## initLicense

Initialize the license of Dynamsoft Capture Vision.

```js
static initlicense(license: string): Promise<void>
```

**Parameters**

`license`: A license key.

**Code Snippet**

```js
try{
  await reader.initLicense("Put-Your-License-Here");
}catch(ex){
  // If the license is not activated, throw an exception.
}
```

## createInstance

Staticly create a barcode reader instance.

```js
static createInstance(): Promise<DynamsoftBarcodeReader>
```

**Return Value**

A barcode reader instance.

**Code Snippet**

```js
let reader = await DynamsoftBarcodeReader.createInstance();
```

## getVersion

Get the version of `DynamsoftBarcodeReader`, which is packaged in Dynamsoft Capture Vision.

```js
getVersion():string Promise<String>
```

**Return Value**

The Version of `DynamsoftBarcodeReader`.

**Code Snippet**

```js
let dbrVersion = await reader.getVersion();
```

## getDBRRuntimeSettings

Get the current runtime settings of `DynamsoftBarcodeReader`.

```js
getRuntimeSettings(): Promise<DBRRuntimeSettings
```

**Return Value**

An object that stores the runtime settings.

**Code Snippet**

```js
let settings = await reader.getDBRRuntimeSettings();
```

## updateDBRRuntimeSettings

Update the barcode decoding settings with a DBRRuntimeSettings struct or a template.

```js
updateRuntimeSettings(settings: RuntimeSettings | string | EnumPresetTemplate): Promise<void>
```

**Parameters**

`Settings`: The parameter should be one of the following types:

- An object that stores barcode reader runtime settings.
- A JSON string that stores the barcode reader template.
- An enumeration member of EnumPresetTemplate

**Code Snippet**

```js
let settings = await reader.getDBRRuntimeSettings();
settings.barcodeFormatIds = EnumBarcodeFormat.BF_ONED;
await reader.updateDBRRuntimeSettings(settings);
```

## resetDBRRuntimeSettings

Reset the barcode decoding settings.

```js
resetRuntimeSettings(): Promise<void>
```

**Code Snippet**

```js
await reader.resetDBRRuntimeSettings();
```

## outputDBRRuntimeSettings

Output the barcode decoding settings to string.

```js
outputRuntimeSettingsToString(): Promise<string>
```

**Return Value**

A string that stores the barcode decoding settings. The barcode settings string can be applied to debug on barcode decoding settings.

**Code Snippet**

```js
let settingString = await reader.outputDBRRuntimeSettings();
```

## startBarcodeScanning

Start the barcode decoding thread.

```js
startScanning(): Promise<void>
```

**Code Snippet**

```js
await reader.startBarcodeScanning();
```

## stopBarcodeScanning

Stop the barcode decoding thread.

```js
stopScanning(): Promise<void>
```

**Code Snippet**

```js
await reader.stopBarcodeScanning();
```

## addFrameListener

Specifies an event handler that fires after the library finishes scanning a frame.

```js

```

**Parameters**

**Return Value**

**Code Snippet**

```js

```
