---
layout: default-layout
title: Class BarcodeLocationResult of Dynamsoft Capture Vision Xamarin Edition
description: The class of barcode location result
keywords: Class BarcodeLocationResult, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: BarcodeLocationResult
---

# BarcodeLocationResult

Class `BarcodeLocationResult`. The location of a quadrilateral area which indicates the location of the detected barcode.

```c#
namespace DCVXamarin
{
    public class BarcodeLocationResult
    {
        // The angle of a barcode. Values range from 0 to 360.
        public int Angle { get; set; }
        
        // The coordinates of the quadrilateral points.
        public Quadrilateral Quadrilateral { get; set; }
    }
}
```

- [`Class BarcodeResult`](class-barcode-result.md)
- [`Class Quadrilateral`](class-quadrilateral.md)
- [`Class Point`](class-point.md)
