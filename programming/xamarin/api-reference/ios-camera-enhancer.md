---
layout: default-layout
title: DCVCameraEnhancer Class under namespace Xamarin.iOS
description: DCVCameraEnhancer class of Xamarin.iOS implements the IDCVCameraEnhancer interface on iOS.
keywords: DCVCameraEnhancer, API reference, Xamarin.iOS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Xamarin.iOS - DCVCameraEnhancer
---

# DCVCameraEnhancer - DCVXamarin.iOS

`DCVCameraEnhancer` class of DCVXamarin.iOS implements interface `IDCVCameraEnhancer` on iOS.

```c#
namespace DCVXamarin.iOS
{
    public class DCVCameraEnhancer : IDCVCameraEnhancer
    {
        public DCVCameraEnhancer();

        public void SetScanRegion(Region region);
        public void ScanRegionVisible(bool isVisible);
        public void Open();
        public void Close();
        public void TurnOnTorch();
        public void TurnOffTorch();
    }
}
```

**Code Snippet**

```c#
DCVCameraEnhancer dce = new DCVCameraEnhancer();
DCVBarcodeReader dbr = new DCVBarcodeReader();
LoadApplication(new App(dce, dbr));
```
