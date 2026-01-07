---
layout: default-layout
title: EnumCapturedResultItemType - Dynamsoft Capture Vision React Native Enumeration
description: Enumeration EnumCapturedResultItemType of Dynamsoft Capture Vision React Native Edition defines the accepted result types that the Capture Vision instance will output.
keywords: captured result, react native, capture vision, settings, barcode reader
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumCapturedResultItemType
---

# EnumCapturedResultItemType

`EnumCapturedResultItemType` is an enumeration that specifies the different types of results that a `CaptureVisionRouter` instance can output. Each functional product under the Capture Vision umbrella has its own unique result type(s). For instance, the Barcode Reader outputs the result type `barcode`, while the Document Normalizer outputs a `detectedQuad` or a `deskewedImage`.

> [!NOTE]
> Although most of the result types are unique to a certain functional product, the `originalImage` result type is shared between all of the functional products.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumCapturedResultItemType {
  CRIT_ORIGINAL_IMAGE = 0x1,
  CRIT_BARCODE = 0x2,
  CRIT_TEXT_LINE = 0x4,
  CRIT_DETECTED_QUAD = 0x8,
  CRIT_DESKEWED_IMAGE = 0x10,
  CRIT_PARSED_RESULT = 0x20,
  CRIT_ENHANCED_IMAGE = 0x40,
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `CRIT_ORIGINAL_IMAGE` | The original image. |
| `CRIT_BARCODE` | The decoded barcode. |
| `CRIT_TEXT_LINE` | The recognized text line. |
| `CRIT_DETECTED_QUAD` | The detected quadrilateral. |
| `CRIT_DESKEWED_IMAGE` | The deskewed image. |
| `CRIT_PARSED_RESULT` | The parsed result. |
| `CRIT_ENHANCED_IMAGE` | The enhanced image. |
