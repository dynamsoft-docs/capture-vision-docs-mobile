---
layout: default-layout
title: EnumCapturedResultItemType - Dynamsoft Barcode Reader Flutter
description: Enumeration EnumCapturedResultItemType of DBR Flutter Edition defines the accepted result types that the Capture Vision instance will output
keywords: captured result, flutter, capture vision, settings, barcode reader
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumCapturedResultItemType
---

# EnumCapturedResultItemType

`EnumCapturedResultItemType` is an enumeration that specifies the different types of results that a `CaptureVisionRouter` instance can output. Each functional product under the Capture Vision umbrella has its own unique result type(s). For instance, the Barcode Reader outputs the result type `barcode`, while the Document Normalizer outputs a `detectedQuad` or a `deskewedImage`.

> [!NOTE]
> Although most of the result types are unique to a certain functional product, the `originalImage` result type is shared between all of the functional products.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
enum EnumCapturedResultItemType {
  originalImage(1),
  barcode(1 << 1),
  textLine(1 << 2),
  detectedQuad(1 << 3),
  deskewedImage(1 << 4),
  parsedResult(1 << 5),
  enhancedImage(1 << 6);
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `originalImage` | The original image. |
| `barcode` | The decoded barcode. |
| `textLine` | The recognized text line. |
| `detectedQuad` | The detected quadrilateral. |
| `deskewedImage` | The deskewed image. |
| `parsedResult` | The parsed result. |
| `enhancedImage` | The enhanced image. |
