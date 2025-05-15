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
> - [DetectedQuadsResult]({{ site.ddn_android_api }}detected-quads-result.html)
> - [NormalizedImagesResult]({{ site.ddn_android_api }}normalized-images-result.html)
> - [ParsedResults]({{ site.dcp_android_api }}parsed-result.html)

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionRouter.aar

```java
class CapturedResult
```

## Attributes

| Method | Description |
| ------ | ----------- |
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Get the hash id of the original image. You can use this ID to get the original image via `IntermediateResultManager` class. |
| [`getOriginalImageTag`](#getoriginalimagetag) | The [ImageTag]({{ site.dcv_android_api }}core/basic-structures/image-tag.html) associated with the original image. |
| [`getItems`](#getitems) | Get an array of `CapturedResultItems`, which are the basic unit of the captured results. A `CapturedResultItem` can be a original image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View CapturedResultItemType for all available types. |
| [`getrotationTransformMatrix`](#getrotationtransformmatrix) | Get the  rotation transformation matrix of the original image relative to the rotated image. |
| [`getErrorCode`](#geterrorcode) | Get the error code associated with the capture result. |
| [`getErrorMessage`](#geterrormessage) | Get the error message associated with the capture result. |
| [`getDecodedBarcodesResult`](#getdecodedbarcodesresult) | Get a [`DecodedBarcodesResult`]({{ site.dbr_android_api }}decoded-barcodes-result.html) object that contains all the [`BarcodeResultItems`]({{ site.dbr_android_api }}barcode-result-item.html) in the `CapturedResult`. |
| [`getRecognizedTextLinesResult`](#getrecognizedtextlinesresult) | Get a [`RecognizedTextLinesResult`]({{ site.dlr_android_api }}recognized-text-lines-result.html) object that contains all the [`TextLineResultItems`]({{ site.dlr_android_api }}text-line-result-item.html) in the `CapturedResult`. |
| [`getDetectedQuadsResult`](#getdetectedquadsresult) | Get a [`DetectedQuadsResult`]({{ site.ddn_android_api }}detected-quads-result.html) object that contains all the [`DetectedQuadResultItem`]({{ site.ddn_android_api }}detected-quad-result-item.html) in the `CapturedResult`. |
| [`getNormalizedImagesResult`](#getnormalizedimagesresult) | Get a [`NormalizedImagesResult`]({{ site.ddn_android_api }}normalized-images-result.html) object that contains all the [`NormalizedImageResultItem`]({{ site.ddn_android_api }}normalized-image-result-item.html) in the `CapturedResult`. |
| [`getParsedResult`](#getparsedresult) | Get the parsed result. |

### getOriginalImageHashId

Get the hash ID of the original image which can be used to get the original image via the [IntermediateResultManager]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/intermediate-result-manager.html) class.

```java
String getOriginalImageHashId();
```

**Return Value**

The hash id of the original image.

### getOriginalImageTag

Get the [ImageTag]({{ site.dcv_android_api }}core/basic-structures/image-tag.html) of the original image that records information such as the image ID of the original image.

```java
ImageTag getOriginalImageTag();
```

**Return Value**

The tag of the original image that records the information of the original image.

### getItems

Get an array of [`CapturedResultItem`]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html), which is the basic unit of the captured results. A [`CapturedResultItem`]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html) can be a original image, a decoded barcode, a recognized text, a detected quad, a normalized image, or a parsed result. View [`CapturedResultItemType`]({{site.dcv_enumerations}}core/captured-result-item-type.html) for all available types.

```java
CapturedResultItem[] getItems();
```

**Return Value**

An array containing the [`CapturedResultItem`]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html) objects within the captured result.

### getRotationTransformMatrix

Get the rotation transformation matrix of the original image relative to the rotated image.

```java
Matrix getRotationTransformMatrix();
```

**Return Value**

Return the rotation transformation matrix of the original image relative to the rotated image.

### getErrorCode

Get the error code if an error occurs when processing the image.

```java
int getErrorCode();
```

### getErrorMessage

Get the error message if an error occurs when processing the image.

```java
String getErrorMessage();
```

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

### getDetectedQuadsResult

Get all the quad detection results of the `CapturedResult`.

```java
DetectedQuadsResult getDetectedQuadsResult();
```

**Return Value**

A [`DetectedQuadsResult`]({{ site.ddn_android_api }}detected-quads-result.html) that contains all the [`DetectedQuadResultItems`]({{ site.ddn_android_api }}detected-quad-result-item.html) of the `CapturedResult`.

### getNormalizedImagesResult

Get all the image normalization results of the `CapturedResult`.

```java
NormalizedImagesResult getNormalizedImagesResult();
```

**Return Value**

A [`NormalizedImagesResult`]({{ site.ddn_android_api }}normalized-images-result.html) that contains all the [`NormalizedImageResultItems`]({{ site.ddn_android_api }}normalized-image-result-item.html) of the `CapturedResult`.

### getParsedResult

Get all the parsed results of the `CapturedResult`.

```java
ParsedResult getParsedResult();
```

**Return Value**

A [`ParsedResult`]({{ site.dcp_android_api }}parsed-result.html) that contains all the [`ParsedResultItems`]({{ site.dcp_android_api }}parsed-result-item.html) of the `CapturedResult`.
