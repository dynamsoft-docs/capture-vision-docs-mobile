---
layout: default-layout
title: Barcode Reader Class of Dynamsoft Capture Vision Flutter Edition
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
| [`getRuntimeSettings`](#getruntimesettings) | Get the current runtime settings of `DynamsoftBarcodeReader`. |
| [`updateRuntimeSettings`](#updateruntimesettings) | Update the runtime settings of `DynamsoftBarcodeReader` with a `DBRRuntimeSettings` struct or a template. |
| [`resetRuntimeSettings`](#resetruntimesettings) | Reset the runtime settings of `DynamsoftBarcodeReader` to default. |
| [`outputRuntimeSettings`](#outputruntimesettings) | Output the runtime settings of `DynamsoftBarcodeReader` to string. |
| [`startScanning`](#startscanning) | Start the barcode decoding thread. |
| [`stopScanning`](#stopscanning) | Stop the barcode decoding thread. |
| [`addResultListener`](#addresultlistener) | Specifies an event handler that fires after the library finishes scanning a frame. |

## initLicense

Initialize the license of Dynamsoft Capture Vision.

```dart
static Future<bool> initLicense({required String license})
```

**Parameters**

`license`: A license key.

**Code Snippet**

```dart
await DynamsoftBarcodeReader.initLicense(license: 'Put-Your-License-Here');
```

## createInstance

Staticly create a barcode reader instance.

```dart
static Future<DynamsoftBarcodeReader> createInstance() async
```

**Return Value**

A barcode reader instance.

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
```

## getVersion

Get the version of `DynamsoftBarcodeReader`, which is packaged in Dynamsoft Capture Vision.

```dart
Future<String> getVersion()
```

**Return Value**

The Version of `DynamsoftBarcodeReader`.

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
String dbrVersion = await _barcodeReader.getVersion();
```

## getRuntimeSettings

Get the current runtime settings of `DynamsoftBarcodeReader`.

```dart
Future<DBRRuntimeSettings> getRuntimeSettings()
```

**Return Value**

An object of [`DBRRuntimeSettings`](class-dbr-runtime-settings.md) that stores the runtime settings.

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
try {
  DBRRuntimeSettings currentSettings = await _barcodeReader.getRuntimeSettings();
} catch (e) {
  print('error = $e');
}
```

## updateRuntimeSettings

Update the barcode decoding settings with a [`DBRRuntimeSettings`](class-dbr-runtime-settings.md) struct or a template.

```dart
Future<void> updateRuntimeSettings({required DBRRuntimeSettings settings})
```

**Parameters**

`Settings`: An object that stores barcode reader runtime settings.

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
try {
  DBRRuntimeSettings settings = await _barcodeReader.getRuntimeSettings();
  // Configure your barcode settings.
  await _barcodeReader.updateRuntimeSettings(settings: settings);
} catch (e) {
  print('error = $e');
}
```

## updateRuntimeSettingsFromTemplate

Update the barcode decoding settings with a preset template.

```dart
Future<void> updateRuntimeSettingsFromTemplate({required EnumDBRPresetTemplate template}) 
```

**Parameters**

`template`: An enumeration member of [`EnumDBRPresetTemplate`](enum-dbr-preset-template.md).

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
await _barcodeReader.updateRuntimeSettingsFromTemplate(template: EnumDBRPresetTemplate.DEFAULT);
```

## updateRuntimeSettingsFromJson

Update the barcode decoding settings with a JSON template.

```dart
Future<void> updateRuntimeSettingsFromJson({required String jsonString})
```

**Parameters**

`jsonString`: An JSON string that includes barcode reader settings.

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
try {
  await _barcodeReader.updateRuntimeSettingsFromJson(jsonString: '**********');
} catch (e) {
  print('error = $e');
}
```

## resetRuntimeSettings

Reset the barcode decoding settings.

```dart
Future<void> resetRuntimeSettings()
```

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
try {
  await _barcodeReader.resetRuntimeSettings();
} catch (e) {
  print('error = $e');
}
```

## outputRuntimeSettingsToString

Output the barcode decoding settings to string.

```dart
Future<String> outputRuntimeSettingsToString()
```

**Return Value**

A string that stores the barcode decoding settings. The barcode settings string can be applied to debug barcode decoding settings.

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
try {
  String settingString = await _barcodeReader.outputRuntimeSettingsToString();
} catch (e) {
  print('error = $e');
}
```

## startScanning

Start the barcode decoding thread.

```dart
Future<void> startScanning()
```

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
await _barcodeReader.startScanning();
```

## stopScanning

Stop the barcode decoding thread.

```dart
Future<void> stopScanning()
```

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
await _barcodeReader.stopScanning();
```

## addResultListener

Specifies an event handler that fires after the library finishes scanning a frame.

```dart
Stream<List<BarcodeResult>> addResultlistener()
```

**Return Value**

Stream that stores a list of [`BarcodeResult`](class-barcode-result.md)

**Code Snippet**

```dart
late final DynamsoftBarcodeReader _barcodeReader;
await DynamsoftBarcodeReader.initLicense(license: '**********');
_barcodeReader = await DynamsoftBarcodeReader.createInstance();
_barcodeReader.startScanning();
_barcodeReader.addResultlistener().listen((List<TextResult> res) {});
```
