---
layout: default-layout
title: Class BarcodeResult of Dynamsoft Capture Vision Flutter Edition
description: The class of BarcodeResult result
keywords: Class BarcodeResult, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: BarcodeResult
---

# BarcodeResult

Class `BarcodeResult`. The return value when a barcode is detected. It stores the barcode information including barcode text and barcode formats.

```dart
class BarcodeResult {
  /// The barcode text.
  final String barcodeText;

  /// Barcode type in string.
  final String barcodeFormatString;

  /// The corresponding localization result.
  final BarcodeLocationResult barcodeLocation;
}
```

## Related API(s)

- [`DynamsoftBarcodeReader.addResultListener`](barcode-reader.md#addresultlistener)
- [`Class BarcodeLocationResult`](class-barcode-location-result.md)
- [`Class Quadrilateral`](class-quadrilateral.md)
- [`Class Point`](class-point.md)
