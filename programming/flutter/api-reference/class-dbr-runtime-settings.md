---
layout: default-layout
title: Class DBRRuntimeSettings of Dynamsoft Capture Vision Flutter Edition
description: The class of DBR runtime settings
keywords: Class DBRRuntimeSettings, API Reference, Flutter
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: DBRRuntimeSettings
---

# DBRRuntimeSettings

Class `DBRRuntimeSettings`. It stores the basic barcode decoding settings when using Dynamsoft Barcode Reader.

```dart
class DBRRuntimeSettings extends Serializer{
    /// Sets the formats of the barcode in BarcodeFormat group 1 to be read. Barcode formats in BarcodeFormat group 1 can be combined.
    int? barcodeFormatIds;

    /// Sets the formats of the barcode in BarcodeFormat group 2 to be read. Barcode formats in BarcodeFormat group 2 can be combined.
    int? barcodeFormatIds_2;

    /// Sets the number of barcodes expected to be detected for each image.
    int? expectedBarcodeCount;

    /// Sets the maximum amount of time (in milliseconds) that should be spent searching for a barcode per page.
    int? timeout;

    /// Filter the barcode results by the minimum length of barcode text.
    int? minBarcodeTextLength;

    /// Filter the barcode results by the minimum confidence.
    int? minResultConfidence;
}
```

## Related API(s)

- [`updateRuntimeSettings`](barcode-reader.md#updateruntimesettings)
- [`EnumBarcodeFormat`](enum-barcode-format.md)
- [`EnumBarcodeFormat_2`](enum-barcode-format2.md)
