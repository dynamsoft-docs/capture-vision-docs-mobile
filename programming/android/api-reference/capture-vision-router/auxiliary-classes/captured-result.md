---
layout: default-layout
title: CapturedResult - Dynamsoft Capture Vision Module Android Edition API Reference
description: The class CapturedResult of Dynamsoft Capture Vision Module represents the result of a capture operation on an image, which contains multiple items such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.
keywords: captured result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResult

The `CapturedResult` class represents the result of a capture operation on an image. Internally, `CapturedResult` stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, original image, parsed item, etc.

> You might also looking for:
>
> - [DecodedBarcodesResult]({{ site.dbr_android_api }}decoded-barcodes-result.html)
> - [RecognizedTextLinesResult]({{ site.dlr_android_api }}recognized-text-lines-result.html)
> - [ProcessedDocumentResult]({{ site.ddn_android_api }}processed-document-result.html)
> - [ParsedResults]({{ site.dcp_android_api }}parsed-result.html)

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class CapturedResult
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getItems`](#getitems) | Get an array of `CapturedResultItems`, which are the basic unit of the captured results. A `CapturedResultItem` can be a original image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View CapturedResultItemType for all available types. |
| [`getDecodedBarcodesResult`](#getdecodedbarcodesresult) | Get a [`DecodedBarcodesResult`]({{ site.dbr_android_api }}decoded-barcodes-result.html) object that contains all the [`BarcodeResultItems`]({{ site.dbr_android_api }}barcode-result-item.html) in the `CapturedResult`. |
| [`getRecognizedTextLinesResult`](#getrecognizedtextlinesresult) | Get a [`RecognizedTextLinesResult`]({{ site.dlr_android_api }}recognized-text-lines-result.html) object that contains all the [`TextLineResultItems`]({{ site.dlr_android_api }}text-line-result-item.html) in the `CapturedResult`. |
| [`getProcessedDocumentResult`](#getprocesseddocumentresult) | Get a [`ProcessedDocumentResult`]({{ site.ddn_android_api }}processed-document-result.html) object that contains all the results with the type of deskewed image, detected quads, and enhanced images. |
| [`getParsedResult`](#getparsedresult) | Get the parsed result. |

The following methods are inherited from [`CapturedResultBase`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html):

| Method | Description |
| ------ | ----------- |
| [`getOriginalImageHashId`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#getoriginalimagehashid) | Gets the hash id of the original image. |
| [`getOriginalImageTag`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#getoriginalimagetag) | Gets the [ImageTag](image-tag.md) of the original image. |
| [`getRotationTransformMatrix`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#getrotationtransformmatrix) | Gets the rotation transformation matrix of the original image relative to the rotated image. |
| [`getErrorCode`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#geterrorcode) | Gets the error code of this result. |
| [`getErrorMessage`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#geterrormessage) | Gets the error message of this result. |

### getItems

Get an array of [`CapturedResultItem`]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html), which is the basic unit of the captured results. A [`CapturedResultItem`]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html) can be a original image, a decoded barcode, a recognized text, a detected quad, a normalized image, or a parsed result. View [`CapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html) for all available types.

```java
CapturedResultItem[] getItems();
```

**Return Value**

An array containing the [`CapturedResultItem`]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html) objects within the captured result.

### getDecodedBarcodesResult

Get all the barcode decoding results of the `CapturedResult`.

```java
DecodedBarcodesResult getDecodedBarcodesResult();
```

**Return Value**

A [`DecodedBarcodesResult`]({{ site.dbr_android_api }}decoded-barcodes-result.html) that contains all the [`BarcodeResultItems`]({{ site.dbr_android_api }}barcode-result-item.html) of the `CapturedResult`.

### getRecognizedTextLinesResult

Get all the text line recognition results of the `CapturedResult`.

```java
RecognizedTextLinesResult getRecognizedTextLinesResult();
```

**Return Value**

A [`RecognizedTextLinesResult`]({{ site.dlr_android_api }}recognized-text-lines-result.html) that contains all the [`TextLineResultItems`]({{ site.dlr_android_api }}text-line-result-item.html) of the `CapturedResult`.

### getProcessedDocumentResult

Get a [`ProcessedDocumentResult`]({{ site.ddn_android_api }}processed-document-result.html) object that contains all the results with the type of deskewed image, detected quads, and enhanced images.

```java
ProcessedDocumentResult getProcessedDocumentResult();
```

**Return Value**

A [`ProcessedDocumentResult`]({{ site.ddn_android_api }}processed-document-result.html) object. It consists of:

- [`DeskewedImageResultItem`]({{ site.ddn_android_api }}deskewed-image-result-item.html)
- [`DetectedQuadResultItem`]({{ site.ddn_android_api }}detected-quad-result-item.html)
- [`EnhancedImageResultItem`]({{ site.ddn_android_api }}enhanced-image-result-item.html)

### getParsedResult

Get all the parsed results of the `CapturedResult`.

```java
ParsedResult getParsedResult();
```

**Return Value**

A [`ParsedResult`]({{ site.dcp_android_api }}parsed-result.html) that contains all the [`ParsedResultItems`]({{ site.dcp_android_api }}parsed-result-item.html) of the `CapturedResult`.
