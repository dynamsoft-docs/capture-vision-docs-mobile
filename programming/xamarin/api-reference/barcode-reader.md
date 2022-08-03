---
layout: default-layout
title: Interface IDCVBarcodeReader of Dynamsoft Capture Vision Xamarin Edition
description: This page is the API reference of Interface IDCVBarcodeReader
keywords: Interface IDCVBarcodeReader, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Interface IDCVBarcodeReader
---

# Interface IDCVBarcodeReader

A barcode reader object accesses to a camera via DynamsoftCameraView object at native level, then perform continuous barcode scanning on the incoming frames.

```c#
interface IDCVBarcodeReader
```

| Method | Description |
| ------- | ----------- |
| [`InitLicense`](#initlicense) | Initialize the license of Dynamsoft Capture Vision. |
| [`GetVersion`](#getversion) | Get the version of `DynamsoftBarcodeReader`, which is packaged in Dynamsoft Capture Vision. |
| [`GetRuntimeSettings`](#getruntimesettings) | Get the current runtime settings of `DynamsoftBarcodeReader`. |
| [`UpdateRuntimeSettings`](#updateruntimesettingsdbrruntimesettings) | Update the runtime settings of `DynamsoftBarcodeReader` with a `DBRRuntimeSettings` struct. |
| [`UpdateRuntimeSettings`](#updateruntimesettingsenumpresettemplate) | Update the runtime settings of `DynamsoftBarcodeReader` with a preset template. |
| [`ResetRuntimeSettings`](#resetruntimesettings) | Reset the runtime settings of `DynamsoftBarcodeReader` to default. |
| [`OutputRuntimeSettings`](#outputruntimesettings) | Output the runtime settings of `DynamsoftBarcodeReader` to string. |
| [`StartScanning`](#startscanning) | Start the barcode decoding thread. |
| [`StopScanning`](#stopscanning) | Stop the barcode decoding thread. |
| [`SetCameraEnhancer`](#setcameraenhancer) | Set camera enhancer as the source of video stream. The library will be able to continuously obtain video frames from the camera enhancer when this method is triggered. |
| [`AddResultListener`](#addresultlistener) | Specifies an event handler that fires after the library finishes scanning a frame. |

## InitLicense

Initialize the license of Dynamsoft Capture Vision.

```c#
void InitLicense(string licenseKey, ILicenseVerificationListener listener)
```

**Parameters**

`licenseKey`: A license key.

**Code Snippet**

```c#
public partial class DBRRendererPage : ContentPage, ILicenseVerificationListener
{
    public DBRRendererPage()
    {
        App.barcodeReader.InitLicense("Put your license key here.", this);
        ...
    }
    ...
    public void ILicenseVerificationListener.LicenseVerificationCallback(bool isSuccess, string msg)
    {
        if (!isSuccess) 
        {
            Console.WriteLine(msg);
        }
    }
}
```

## GetVersion

Get the version of `DynamsoftBarcodeReader`, which is packaged in Dynamsoft Capture Vision.

```c#
string GetVersion()
```

**Return Value**

The Version of `DynamsoftBarcodeReader`.

## GetRuntimeSettings

Get the current runtime settings of `DynamsoftBarcodeReader`.

```c#
DBRRuntimeSettings GetRuntimeSettings()
```

**Return Value**

An object of [`DBRRuntimeSettings`](class-dbr-runtime-settings.md) that stores the runtime settings.

**Code Snippet**

```c#
DBRRuntimeSettings settings = App.barcodeReader.GetRuntimeSettings();
settings.BarcodeFormatIds = EnumBarcodeFormat.BF_CODE_128 | EnumBarcodeFormat.BF_QR_CODE;
settings.ExpectedBarcodeCount = 0;
settings.Timeout = 300;
App.barcodeReader.UpdateRuntimeSettings(settings);
```

## UpdateRuntimeSettings(DBRRuntimeSettings)

Update the barcode decoding settings with a [`DBRRuntimeSettings`](class-dbr-runtime-settings.md) struct or a template.

```c#
void UpdateRuntimeSettings(DBRRuntimeSettings settings)
```

**Parameters**

`Settings`: An object that stores barcode reader runtime settings.

**Code Snippet**

```c#
DBRRuntimeSettings settings = App.barcodeReader.GetRuntimeSettings();
settings.BarcodeFormatIds = EnumBarcodeFormat.BF_CODE_128 | EnumBarcodeFormat.BF_QR_CODE;
settings.ExpectedBarcodeCount = 0;
settings.Timeout = 300;
App.barcodeReader.UpdateRuntimeSettings(settings);
```

## UpdateRuntimeSettings(EnumPresetTemplate)

Update the barcode decoding settings with a preset template.

```c#
void UpdateRuntimeSettingsFromTemplate(EnumDBRPresetTemplate template)
```

**Parameters**

`template`: An enumeration member of [`EnumDBRPresetTemplate`](enum-dbr-preset-template.md).

**Code Snippet**

```c#
App.barcodeReader.UpdateRuntimeSettings(EnumDBRPresetTemplate.VIDEO_SINGLE_BARCODE);
```

## UpdateRuntimeSettings(String)

Update the barcode decoding settings with a JSON template.

```c#
void UpdateRuntimeSettingsFromTemplate(string jsonTemplate)
```

**Parameters**

`jsonString`: An JSON string that includes barcode reader settings.

**Code Snippet**

```c#
App.barcodeReader.UpdateRuntimeSettings("{\"ImageParameter\":{\"BarcodeFormatIds\":[\"BF_ALL\"],\"BarcodeFormatIds_2\":null,\"DeblurLevel\":0,\"ExpectedBarcodesCount\":0,\"LocalizationModes\":[{\"Mode\":\"LM_SCAN_DIRECTLY\",\"ScanDirection\":1},{\"Mode\":\"LM_CONNECTED_BLOCKS\"}],\"Name\":\"video-speed-first\",\"ScaleDownThreshold\":2300,\"Timeout\":500},\"Version\":\"3.0\"}");
```

## ResetRuntimeSettings

Reset the barcode decoding settings to default value.

```c#
void ResetRuntimeSettings()
```

## OutputRuntimeSettingsToString

Output the barcode decoding settings to string.

```c#
string OutputRuntimeSettingsToString()
```

**Return Value**

A string that stores the barcode decoding settings. The barcode settings string can be applied to debug barcode decoding settings.

## StartScanning

Start the barcode decoding thread.

```c#
void StartScanning()
```

## StopScanning

Stop the barcode decoding thread.

```c#
void StopScanning()
```

## SetCameraEnhancer

Set camera enhancer as the source of video stream. The library will be able to continuously obtain video frames from the camera enhancer when this method is triggered.

```c#
void SetCameraEnhancer(IDCVCameraEnhancer dce);
```

**Parameters**

`dce`: An instance of `IDCVCameraEnhancer`.

**Code Snippet**

```c#
App.dbr.SetCameraEnhancer(App.dce);
```

## AddResultListener

Specifies an event handler that fires after the library finishes scanning a frame.

```c#
void AddResultlistener(IBarcodeResultListener listener)
```

**Code Snippet**

The following code snippet shows how to use barcode reader module to decode from video stream.

```c#
// Add IBarcodeResultListener to your page class
public partial class DBRRendererPage : ContentPage, IBarcodeResultListener
{
    public DBRRendererPage()
    {
        // Add the result listener so that you can receive the barcode results from the BarcodeResultCallback.
        App.barcodeReader.AddResultListener(this);
        // You have to set camera enhancer as the video source to decode from video stream.
        App.barcodeReader.SetCameraEnhancer();
        ...
    }
    ...
    protected override void OnAppearing()
    {
        base.OnAppearing();
        // Open the camera.
        App.camera.Open();
        // Start the barcode decoding thread.
        App.barcodeReader.StartScanning();
    }

    protected override void OnDisappearing()
    {
        base.OnDisappearing();
        App.camera.Close();
        App.barcodeReader.StopScanning();
    }
    public void BarcodeResultCallback(BarcodeResult[] barcodeResults)
    {
        // Add your code to execute here when barcode results are received.
    }
}
```
