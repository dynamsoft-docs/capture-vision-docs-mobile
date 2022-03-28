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

# Barcode Reader Class

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
static initlicense(): Promise<void>
```

**Parameters**

A license key.

**Return Value**

**Code Snippet**

## createInstance

Create a barcode reader instance.

```js
static createInstance(): Promise<DynamsoftBarcodeReader>
```

## getVersion

Get the version of `DynamsoftBarcodeReader`, which is packaged in Dynamsoft Capture Vision.

```js
getVersion():string Promise<String>
```

**Return Value**

The Version of `DynamsoftBarcodeReader`.

**Code Snippet**

## getDBRRuntimeSettings

Get the current runtime settings of `DynamsoftBarcodeReader`.

```js
getRuntimeSettings(): Promise<DBRRuntimeSettings
```

**Return Value**

An object that stores the runtime settings.

**Code Snippet**

## updateDBRRuntimeSettings

Update the barcode decoding settings with a DBRRuntimeSettings struct or a template.

```js
updateRuntimeSettings(settings: RuntimeSettings | string | EnumPresetTemplate): Promise<void>
```

**Parameters**

The parameter should be one of the following types:

- An object that stores barcode reader runtime settings.
- A JSON string that stores the barcode reader template.
- An enumeration member of EnumPresetTemplate

**Code Snippet**

## resetDBRRuntimeSettings

Reset the barcode decoding settings.

```js
resetRuntimeSettings(): Promise<void>
```

**Code Snippet**

## outputDBRRuntimeSettings

Output the barcode decoding settings to string.

```js
outputRuntimeSettingsToString(): Promise<string>
```

**Return Value**

A string that stores the barcode decoding settings.

**Code Snippet**

## startBarcodeScanning

Start the barcode decoding thread.

```js
startScanning(): Promise<void>
```

**Code Snippet**

## stopBarcodeScanning

Stop the barcode decoding thread.

```js
stopScanning(): Promise<void>
```

**Code Snippet**

## addFrameListener

Specifies an event handler that fires after the library finishes scanning a frame.

```js

```

**Parameters**

**Return Value**

**Code Snippet**
