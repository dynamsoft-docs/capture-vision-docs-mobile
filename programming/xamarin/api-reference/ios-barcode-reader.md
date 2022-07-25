---
layout: default-layout
title: DCVBarcodeReader Class under namespace Xamarin.iOS
description: DCVBarcodeReader class of Xamarin.iOS implements the IDCVBarcodeReader interface on iOS.
keywords: DCVBarcodeReader, API reference, Xamarin.iOS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Xamarin.iOS - DCVBarcodeReader
---

# DCVBarcodeReader - DCVXamarin.iOS

`DCVBarcodeReader` class of DCVXamarin.iOS implements interface `IDCVBarcodeReader` on iOS.

```c#
namespace DCVXamarin.Droid
{
    public class DCVBarcodeReaderService : Java.Lang.Object, IDCVBarcodeReader, ITextResultListener, IJavaObject, IDisposable, IJavaPeerable, IDBRLicenseVerificationListener
    {
        public DCVBarcodeReaderService();
        // Methods for license Activation
        public void InitLicense(string license, ILicenseVerificationListener listener);
        public void DBRLicenseVerificationCallback(bool p0, Java.Lang.Exception p1);

        // Methods for version check
        public string GetVersion();

        // Methods for video barcode decoding.
        public void BindCameraEnhancer();
        public void StartScanning();
        public void StopScanning();
        public void AddResultlistener(IBarcodeResultListener listener);
        public void TextResultCallback(int i, ImageData p1, TextResult[] results);
        
        // Methods for configuring runtime settings.
        public DBRRuntimeSettings GetRuntimeSettings();
        public void UpdateRuntimeSettings(DBRRuntimeSettings settings);
        public void UpdateRuntimeSettings(EnumDBRPresetTemplate presetTemplate);
        public void UpdateRuntimeSettings(string jsonTemplate);
        public string OutputRuntimeSettingsToString();
        public void ResetRuntimeSettings();
    }
}
```

**Code Snippet**

```c#
DCVCameraEnhancer dce = new DCVCameraEnhancer();
DCVBarcodeReader dbr = new DCVBarcodeReader();
LoadApplication(new App(dce, dbr));
```
