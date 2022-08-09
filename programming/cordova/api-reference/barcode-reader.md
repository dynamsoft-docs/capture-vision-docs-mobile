---
layout: default-layout
title: Class DCVBarcodeReader of Dynamsoft Capture Vision Cordova Edition
description: This page is the API reference of Class DCVBarcodeReader
keywords: Class DCVBarcodeReader, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Class DCVBarcodeReader
---

# Class DCVBarcodeReader

A barcode reader object accesses to a camera via DynamsoftCameraView object at native level, then perform continuous barcode scanning on the incoming frames.

```js
interface DCVBarcodeReader
```

| Method | Description |
| ------- | ----------- |
| [`createInstance`](#createinstance) | Create an instance of `DCVBarcodeReader`. |
| [`initLicense`](#initLicense) | Initialize the license of Dynamsoft Barcode Reader. |
| [`getVersion`](#getversion) | Get the version of `DynamsoftBarcodeReader`, which is packaged in Dynamsoft Capture Vision. |
| [`getRuntimeSettings`](#getruntimesettings) | Get the current runtime settings of `DynamsoftBarcodeReader`. |
| [`updateRuntimeSettings`](#updateruntimesettings) | Update the runtime settings of `DynamsoftBarcodeReader` with a DBRRuntimeSettings object, a preset template or a JSON String. |
| [`resetRuntimeSettings`](#resetruntimesettings) | Reset the runtime settings of `DynamsoftBarcodeReader` to default. |
| [`outputRuntimeSettings`](#outputruntimesettings) | Output the runtime settings of `DynamsoftBarcodeReader` to string. |
| [`startScanning`](#startscanning) | Start the barcode decoding thread. |
| [`stopScanning`](#stopscanning) | Stop the barcode decoding thread. |
| [`addResultListener`](#addresultlistener) | Specifies an event handler that fires after the library finishes scanning a frame. |

## createInstance

Create an instance of `DCVBarcodeReader`.

```js
static createInstance(): Promise<DCVBarcodeReader>;
```

**Return Value**

An instance of `DCVBarcodeReader`.

**Code Snippet**

```js
```

## initLicense

Initialize the license of Barcode Reader module.

```js
static initLicense(license: String): Promise<void>;  
```

**Parameters**

`license`: A license key.

**Code Snippet**

```js
```

## getVersion

Get the version of `DynamsoftBarcodeReader`, which is packaged in Dynamsoft Capture Vision.

```js
static getVersion(): Promise<string>;
```

**Return Value**

The Version of `DynamsoftBarcodeReader`.

## getRuntimeSettings

Get the current runtime settings of `DynamsoftBarcodeReader`.

```js
getRuntimeSettings(): Promise<DBRRuntimeSettings>;
```

**Return Value**

An object of [`DBRRuntimeSettings`](class-dbr-runtime-settings.md) that stores the runtime settings.

**Code Snippet**

```js
```

## updateRuntimeSettings

Update the barcode decoding settings with a [`DBRRuntimeSettings`](class-dbr-runtime-settings.md) struct, a preset template or a JSON String.

```js
updateRuntimeSettings(settings: String | DBRRuntimeSettings | EnumDBRPresetTemplate): Promise<void>;
```

**Parameters**

`settings (DBRRuntimeSettings)`: An object that stores `DBRRuntimeSettings`.  
`settings (EnumDBRPresetTemplate)`: One of the `EnumDBRPresetTemplate` member that indicates a preset template.  
`settings (String)`: A stringified JSON data that contains barcode decoding settings. The available settings include but not limited in `DBRRuntimeSettings`. You can access full feature of DBR when upload the settings from a JSON data.

**Code Snippet**

```js
//App.barcodeReader.UpdateRuntimeSettings("{\"ImageParameter\":{\"BarcodeFormatIds\":[\"BF_ALL\"],\"BarcodeFormatIds_2\":null,\"DeblurLevel\":0,\"ExpectedBarcodesCount\":0,\"LocalizationModes\":[{\"Mode\":\"LM_SCAN_DIRECTLY\",\"ScanDirection\":1},{\"Mode\":\"LM_CONNECTED_BLOCKS\"}],\"Name\":\"video-speed-first\",\"ScaleDownThreshold\":2300,\"Timeout\":500},\"Version\":\"3.0\"}");
```

## resetRuntimeSettings

Reset the barcode decoding settings to default value.

```js
resetRuntimeSettings(): void;
```

## outputRuntimeSettingsToString

Output the barcode decoding settings to string.

```js
outputRuntimeSettingsToString(): Promise<string>;
```

**Return Value**

A string that stores the barcode decoding settings. The barcode settings string can be applied to debug barcode decoding settings.

## startScanning

Start the barcode decoding thread.

```js
startScanning(): void;
```

## stopScanning

Stop the barcode decoding thread.

```js
stopScanning(): void;
```

## AddResultListener

Specifies an event handler that fires after the library finishes scanning a frame.

```js
addResultListener(listener: (results: BarcodeResult[]) => void): void;
```

**Code Snippet**

The following code snippet shows how to use barcode reader module to decode from video stream.

```js
```
