---
layout: default-layout
title: CameraEnhancer Class under namespace Xamarin.iOS
description: CameraEnhancer class of Xamarin.iOS implements the ICameraEnhancer interface on iOS.
keywords: CameraEnhancer, API reference, Xamarin.iOS
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Xamarin.iOS - CameraEnhancer
---

# CameraEnhancer - DCVXamarin.iOS

`CameraEnhancer` class of DCVXamarin.iOS implements interface `ICameraEnhancer` on iOS.

```c#
namespace DCVXamarin.iOS
{
    public class CameraEnhancer : ICameraEnhancer
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
