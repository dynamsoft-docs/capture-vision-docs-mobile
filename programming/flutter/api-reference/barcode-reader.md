---
layout: default-layout
title: DCVBarcodeReader Class of Dynamsoft Capture Vision Flutter Edition
description: This page is the API reference of DCVBarcodeReader class
keywords: Barcode, API reference, Flutter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: DCVBarcodeReader class
---

# DCVBarcodeReader Class

A barcode reader object accesses to a camera via `DCVCameraView` object at native level, then perform continuous barcode scanning on the incoming frames.

| Methods | Description |
| ------- | ----------- |
| [`initLicense`](#initlicense) | Initialize the license of Dynamsoft Capture Vision. |
| [`createInstance`](#createinstance) | Create a barcode reader instance. |
| [`getVersion`](#getversion) | Get the version of `DCVBarcodeReader`, which is packaged in Dynamsoft Capture Vision. |
| [`getRuntimeSettings`](#getruntimesettings) | Get the current runtime settings of `DCVBarcodeReader`. |
| [`updateRuntimeSettings`](#updateruntimesettings) | Update the runtime settings of `DCVBarcodeReader` with a `DBRRuntimeSettings` struct or a template. |
| [`resetRuntimeSettings`](#resetruntimesettings) | Reset the runtime settings of `DCVBarcodeReader` to default. |
| [`outputRuntimeSettingsToString`](#outputruntimesettingstostring) | Output the runtime settings of `DCVBarcodeReader` to string. |
| [`startScanning`](#startscanning) | Start the barcode decoding thread. |
| [`stopScanning`](#stopscanning) | Stop the barcode decoding thread. |
| [`receiveResultStream`](#receiveresultstream) | Receive the stream to listen all the barcode results after the library finishes scanning a frame. |
| [`decodeFile`](#decodefile) | Decode barcodes from an image file. |
| [`enableResultVerification`](#enableresultverification) | Enable result verification. The output result will be double-checked to make sure the accuracy. |

## initLicense

Initialize the license of Dynamsoft Capture Vision.

```dart
static Future<bool> initLicense(String license)
```

**Parameters**

`license`: A license key.

**Code Snippet**

```dart
try {
    await DCVBarcodeReader.initLicense('Put-Your-License-Here');
} catch (e) {
    print('license error = $e');
}
```

## createInstance

Create a barcode reader instance.

```dart
static Future<DCVBarcodeReader> createInstance() async
```

**Return Value**

A barcode reader instance.

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
```

## getVersion

Get the version of `DCVBarcodeReader`, which is packaged in Dynamsoft Capture Vision.

```dart
Future<String?> getVersion()
```

**Return Value**

The Version of `DCVBarcodeReader`.

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
String dbrVersion = await _barcodeReader.getVersion();
```

## getRuntimeSettings

Get the current runtime settings of `DCVBarcodeReader`.

```dart
Future<DBRRuntimeSettings> getRuntimeSettings()
```

**Return Value**

An object of [`DBRRuntimeSettings`](class-dbr-runtime-settings.md) that stores the runtime settings.

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
try {
  DBRRuntimeSettings currentSettings = await _barcodeReader.getRuntimeSettings();
} catch (e) {
  print('error = $e');
}
```

## updateRuntimeSettings

Update the barcode decoding settings with a [`DBRRuntimeSettings`](class-dbr-runtime-settings.md) struct.

```dart
Future<void> updateRuntimeSettings(DBRRuntimeSettings settings)
```

**Parameters**

`Settings`: An object that stores barcode reader runtime settings.

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
try {
  DBRRuntimeSettings settings = await _barcodeReader.getRuntimeSettings();
  // Configure your barcode settings.
  await _barcodeReader.updateRuntimeSettings(settings);
} catch (e) {
  print('error = $e');
}
```

## updateRuntimeSettingsFromTemplate

Update the barcode decoding settings with a preset template.

```dart
Future<void> updateRuntimeSettingsFromTemplate(EnumDBRPresetTemplate template) 
```

**Parameters**

`template`: An enumeration member of [`EnumDBRPresetTemplate`](enum-dbr-preset-template.md).

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
await _barcodeReader.updateRuntimeSettingsFromTemplate(EnumDBRPresetTemplate.DEFAULT);
```

## updateRuntimeSettingsFromJson

Update the barcode decoding settings with a JSON template.

```dart
Future<void> updateRuntimeSettingsFromJson(String jsonString)
```

**Parameters**

`jsonString`: An JSON string that includes barcode reader settings.

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
try {
  await _barcodeReader.updateRuntimeSettingsFromJson("{\"ImageParameter\":{\"BarcodeFormatIds\":[\"BF_ALL\"],\"BarcodeFormatIds_2\":null,\"DeblurLevel\":0,\"ExpectedBarcodesCount\":0,\"LocalizationModes\":[{\"Mode\":\"LM_SCAN_DIRECTLY\",\"ScanDirection\":1},{\"Mode\":\"LM_CONNECTED_BLOCKS\"}],\"Name\":\"video-speed-first\",\"ScaleDownThreshold\":2300,\"Timeout\":500},\"Version\":\"3.0\"}");
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
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
try {
  await _barcodeReader.resetRuntimeSettings();
} catch (e) {
  print('error = $e');
}
```

## outputRuntimeSettingsToString

Output the barcode decoding settings to string.

```dart
Future<String?> outputRuntimeSettingsToString()
```

**Return Value**

A string that stores the barcode decoding settings. The barcode settings string can be applied to debug barcode decoding settings.

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
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
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
await _barcodeReader.startScanning();
```

## stopScanning

Stop the barcode decoding thread.

```dart
Future<void> stopScanning()
```

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
await _barcodeReader.stopScanning();
```

## receiveResultStream

Receive the stream to listen all the barcode results after the library finishes scanning a frame.

```dart
Stream<List<BarcodeResult>> receiveResultStream()
```

**Return Value**

Stream that stores a list of [`BarcodeResult`](class-barcode-result.md)

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
_barcodeReader.startScanning();
_barcodeReader.receiveResultStream().listen((List<BarcodeResult> res) {});
```

## decodeFile

Decode barcodes from an image file.

```dart
Future<List<BarcodeResult>> decodeFile(String path)
```

**Parameters**

`path`: The Path of the image file.

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
final result = await _barcodeReader.decodeFile("Your file path");
```

## enableResultVerification

Enable result verification. The output result will be double-checked to make sure the accuracy.

```dart
Future enableResultVerification(bool isEnable)
```

**Parameters**

`isEnable`: Set the bool value to true to enable the result verification.

**Code Snippet**

```dart
late final DCVBarcodeReader _barcodeReader;
_barcodeReader = await DCVBarcodeReader.createInstance();
_barcodeReader.enableResultVerification(true);
```
