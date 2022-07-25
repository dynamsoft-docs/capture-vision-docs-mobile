---
layout: default-layout
title: DCVCameraEnhancer Class under namespace Xamarin.Droid
description: DCVCameraEnhancer class of Xamarin.Droid implements the IDCVCameraEnhancer interface on Android.
keywords: DCVCameraEnhancer, API reference, Xamarin.Droid
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Xamarin.Droid - DCVCameraEnhancer
---

# DCVCameraEnhancer - DCVXamarin.Droid

`DCVCameraEnhancer` class of DCVXamarin.Droid implements interface `IDCVCameraEnhancer` on Android.

```c#
namespace DCVXamarin.Droid
{
    public class DCVCameraEnhancer : Object, IDCVCameraEnhancer
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
