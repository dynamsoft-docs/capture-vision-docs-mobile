---
layout: default-layout
title: DCVBarcodeReader Class under namespace Xamarin.Droid
description: DCVBarcodeReader class of Xamarin.Droid implements the IDCVBarcodeReader interface on Android.
keywords: DCVBarcodeReader, API reference, Xamarin.Droid
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Xamarin.Droid - DCVBarcodeReader
---

# DCVBarcodeReader - DCVXamarin.Droid

`DCVBarcodeReader` class of DCVXamarin.Droid implements interface `IDCVBarcodeReader` on Android.

```c#
namespace DCVXamarin.Droid
{
    public class DCVBarcodeReader : Java.Lang.Object, IDCVBarcodeReader, ITextResultListener, IJavaObject, IDisposable, IJavaPeerable, IDBRLicenseVerificationListener
    {
        public DCVBarcodeReaderService();
        // Methods for license Activation
        public void InitLicense(string license, ILicenseVerificationListener listener);
        public void DBRLicenseVerificationCallback(bool p0, Java.Lang.Exception p1);

        // Methods for version check
        public string GetVersion();

        // Methods for video barcode decoding.
        public void SetCameraEnhancer();
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
