---
layout: default-layout
title: CapturedResultItem Class - Dynamsoft Capture Vision Flutter
description: CapturedResultItem class of DCV Flutter edition represents the result of a capture operation on an image.
keywords: decoded barcode, parsed result, error code, output, captured result, flutter, barcode reader
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultItem

The `CapturedResultItem` class represents the most basic item in the captured result. Depending on the type of the [`CapturedResult`](captured-result.md), the captured result item can be a barcode, a text line, a normalized image, a detected quad, a parsed item, or an original image.

> [!NOTE]
>
> - Barcode: [BarcodeResultItem]({{ site.dbr_flutter_api }}barcode-reader/barcode-result-item.html)
> - Text line: [`TextLineResultItem`]({{ site.dlr_flutter_api }}text-line-result-item.html)
> - Document page(s): 
>   - [`DeskewedImageResultItem`]({{ site.ddn_flutter_api }}deskewed-image-result-item.html)
>   - [`DetectedQuadResultItem`]({{ site.ddn_flutter_api }}detected-quad-result-item.html)
>   - [`EnhancedImageResultItem`]({{ site.ddn_flutter_api }}enhanced-image-result-item.html)
> - Parsed content (DL, MRZ, VIN, GS1 AI, etc.): [`ParsedResultItem`]({{ site.dcp_flutter_api }}parsed-result-item.html)

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class CapturedResultItem
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`targetROIDefName`](#targetroidefname) | *String* | The name of the target region of interest (ROI) where the captured result was found. |
| [`taskName`](#taskname) | *String* | The name of the recognition task that produced the CapturedResultItem. |
| [`type`](#type) | [*EnumCapturedResultItemType*](enum/captured-result-item-type.md) | The type of the captured result item. |

### targetROIDefName

Returns a string that represents the name of the target region of interest (ROI) where the captured result was found. The target ROI is where the recognition task is run, and it is defined in the Capture Vision template.

```dart
String targetROIDefName,
```

**Remarks**

To learn more about the `TargetROIDef` object, please visit this [page]({{ site.parameter }}file/target-roi-definition/index.html?product=dbr&lang=objectivec-swift).

### taskName

Returns the name of the recognition task that produced the CapturedResultItem. The task name sets the functional product that will be used for the recognition task, and it is defined in the Capture Vision template. 

```dart
String taskName;
```

**Remarks**

To learn more about how the tasks are set in the TargetROIDef object, please visit this [page]({{ site.parameter }}reference/target-roi-def/task-setting-name-array.html?product=dbr&lang=objectivec-swift).

### type

The type of the captured result item represented as a [`EnumCapturedResultItemType`](enum/captured-result-item-type.md). Depending on the functional product used, the captured result item can be a barcode, a text line, a normalized image, a detected quad, a parsed item, or an original image.

```dart
EnumCapturedResultItemType type;
```

**Remarks**

The type of `CapturedResultItem` is dependent on the functional product that is used by the Capture Vision Router instance. To learn about the different types of functional products that Capture Vision supports, please visit the [Capture Vision Introduction]({{ site.introduction }}index.html#functional-products)
