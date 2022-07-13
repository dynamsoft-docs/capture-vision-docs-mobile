---
layout: default-layout
title: CameraEnhancer Class under Name space Xamarin.Droid
description: CameraEnhancer class of Xamarin.Droid implements the ICameraEnhancer interface on Android.
keywords: CameraEnhancer, API reference, Xamarin.Droid
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Xamarin.Droid - CameraEnhancer
---

# CameraEnhancer - DCVXamarin.Droid

`CameraEnhancer` class of DCVXamarin.Droid implements interface `ICameraEnhancer` on Android.

```c#
namespace DCVXamarin.Droid
{
    public class CameraEnhancer : Object, ICameraEnhancer
    {
        public CameraEnhancer();

        public void SetScanRegion(Region region);
        public void ScanRegionVisible(bool isVisible);
        public void Open();
        public void Close();        
        public void TurnOnTorch();
        public void TurnOffTorch();
    }
}
```
