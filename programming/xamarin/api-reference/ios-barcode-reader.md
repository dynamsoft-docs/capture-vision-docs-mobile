---
layout: default-layout
title: BarcodeReader Class under Name space Xamarin.iOS
description: BarcodeReader class of Xamarin.iOS implements the IBarcodeReader interface on iOS.
keywords: BarcodeReader, API reference, Xamarin.iOS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Xamarin.iOS - BarcodeReader
---

# BarcodeReader - DCVXamarin.iOS

`BarcodeReader` class of DCVXamarin.iOS implements interface `IBarcodeReader` on iOS.

```c#
namespace DCVXamarin.Droid
{
    public class BarcodeReaderService : Java.Lang.Object, IBarcodeReader, ITextResultListener, IJavaObject, IDisposable, IJavaPeerable, IDBRLicenseVerificationListener
    {
        public BarcodeReaderService();
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
