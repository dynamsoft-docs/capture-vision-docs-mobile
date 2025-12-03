---
layout: default-layout
title: CapturedResultItem - Dynamsoft Capture Vision React Native
description: Interface CapturedResultItem of DCV React Native edition represents the result of a capture operation on an image.
keywords: decoded barcode, parsed result, error code, output, captured result, react native, barcode reader
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultItem

Interface `CapturedResultItem` represents the most basic item in the captured result. Depending on the type of the [`CapturedResult`](../capture-vision-router/captured-result.md), the captured result item can be a barcode, a text line, a normalized image, a detected quad, a parsed item, or an original image.

> [!NOTE]
> Hierarchy:
> - `CapturedResultItem`
>   - [`BarcodeResultItem`]({{ site.dbr_react_native_api }}barcode-reader/barcode-result-item.html)
>   - [`TextLineResultItem`]({{ site.dlr_react_native_api }}text-line-result-item.html)
>   - [`DeskewedImageResultItem`]({{ site.ddn_react_native_api }}deskewed-image-result-item.html)
>   - [`DetectedQuadResultItem`]({{ site.ddn_react_native_api }}detected-quad-result-item.html)
>   - [`EnhancedImageResultItem`]({{ site.ddn_react_native_api }}enhanced-image-result-item.html)
>   - [`ParsedResultItem`]({{ site.dcp_react_native_api }}parsed-result-item.html)

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface CapturedResultItem
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`targetROIDefName`](#targetroidefname) | *string* | The name of the target region of interest (ROI) where the captured result was found. |
| [`taskName`](#taskname) | *string* | The name of the recognition task that produced the CapturedResultItem. |
| [`type`](#type) | [*EnumCapturedResultItemType*](enum/captured-result-item-type.md) | The type of the captured result item. |

### targetROIDefName

Returns a string that represents the name of the target region of interest (ROI) where the captured result was found. The target ROI is where the recognition task is run, and it is defined in the Capture Vision template.

```js
targetROIDefName?: string;
```

**Remarks**

To learn more about the `TargetROIDef` object, please visit this [page]({{ site.parameter }}file/target-roi-definition/index.html?product=dbr&lang=objectivec-swift).

### taskName

Returns the name of the recognition task that produced the CapturedResultItem. The task name sets the functional product that will be used for the recognition task, and it is defined in the Capture Vision template. 

```js
taskName?: string;
```

**Remarks**

To learn more about how the tasks are set in the TargetROIDef object, please visit this [page]({{ site.parameter }}reference/target-roi-def/task-setting-name-array.html?product=dbr&lang=objectivec-swift).

### type

The type of the captured result item represented as a [`EnumCapturedResultItemType`](enum/captured-result-item-type.md). Depending on the functional product used, the captured result item can be a barcode, a text line, a normalized image, a detected quad, a parsed item, or an original image.

```js
type: EnumCapturedResultItemType | number;
```

**Remarks**

| CapturedResultItemType | Interface |
| ---------------------- | --------- |
| `CRIT_BARCODE` | [`BarcodeResultItem`]({{ site.dbr_react_native_api }}barcode-reader/barcode-result-item.html) |
| `CRIT_TEXT_LINE` | [`TextLineResultItem`]({{ site.dlr_react_native_api }}text-line-result-item.html) |
| `CRIT_DETECTED_QUAD` | [`DetectedQuadResultItem`]({{ site.ddn_react_native_api }}detected-quad-result-item.html) |
| `CRIT_DESKEWED_IMAGE` | [`DeskewedImageResultItem`]({{ site.ddn_react_native_api }}deskewed-image-result-item.html) |
| `CRIT_PARSED_RESULT` | [`ParsedResultItem`]({{ site.dcp_react_native_api }}parsed-result-item.html) |
| `CRIT_ENHANCED_IMAGE` | [`EnhancedImageResultItem`]({{ site.ddn_react_native_api }}enhanced-image-result-item.html) |
