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
namespace DCVXamarin.iOS
{
    public class DCVBarcodeReader : NSObject, IDBRTextResultListener, INativeObject, IDisposable, IDBRLicenseVerificationListener, IDCVBarcodeReader
    {
        public DCVBarcodeReader();

        public void AddResultlistener(IBarcodeResultListener listener);
        public void DBRLicenseVerificationCallback(bool isSuccess, NSError error);
        public DBRRuntimeSettings GetRuntimeSettings();
        public string GetVersion();
        public void InitLicense(string license, ILicenseVerificationListener listener);
        public string OutputRuntimeSettingsToString();
        public void ResetRuntimeSettings();
        public void SetCameraEnhancer(IDCVCameraEnhancer dce);
        public void StartScanning();
        public void StopScanning();
        public void TextResultCallback(nint frameId, iImageData imageData, iTextResult[] results);
        public void UpdateRuntimeSettings(DBRRuntimeSettings settings);
        public void UpdateRuntimeSettings(EnumDBRPresetTemplate presetTemplate);
        public void UpdateRuntimeSettings(string jsonTemplate);
    }
}
```

**Code Snippet**

```c#
DCVCameraEnhancer dce = new DCVCameraEnhancer();
DCVBarcodeReader dbr = new DCVBarcodeReader();
LoadApplication(new App(dce, dbr));
```
