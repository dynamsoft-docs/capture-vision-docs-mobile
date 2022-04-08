---
layout: default-layout
title: Class BarcodeLocationResult of Dynamsoft Capture Vision Flutter Edition
description: The class of barcode location result
keywords: Class BarcodeLocationResult, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: BarcodeLocationResult
---

# BarcodeLocationResult

Class `BarcodeLocationResult`. The location of a quadrilateral area. It can be the location of a decoded barcode, a recognized label or a deteced document area

```dart
class BarcodeLocationResult {
  /// The angle of a barcode. Values range from 0 to 360.
  final int angle;

  /// The coordinates of the quadrilateral points.
  final Quadrilateral location;
}
```

- [`Class BarcodeResult`](class-barcode-result.md)
- [`Class Quadrilateral`](class-quadrilateral.md)
- [`Class Point`](class-point.md)
