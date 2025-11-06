---
layout: default-layout
title: CapturedResult Class - Dynamsoft Capture Vision Flutter
description: CapturedResult class of DCV Flutter edition represents the result of a capture operation on an image.
keywords: decoded barcode, parsed result, error code, output, captured result, flutter, barcode reader
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResult

The `CapturedResult` class represents the result of a capture operation on an image. Internally, `CapturedResult` stores an array of [`CapturedResultItem`](captured-result-item.md), each of which may be a barcode, text line, detected quad, normalized image, original image, or parsed item depending on the functional product that is used.

> [!TIP]
> In the context of the Barcode Reader, you will most likely be using the [`DecodedBarcodesResult`]({{ site.dbr_flutter_api }}barcode-reader/decoded-barcodes-result.html) as the main result type. 

> [!NOTE]
> The type of `CapturedResult` is dependent on the functional product that is used by the Capture Vision Router instance. To learn about the different types of functional products that Capture Vision supports, please visit the [Capture Vision Introduction]({{ site.introduction }}index.html#functional-products).

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class CapturedResult
```

## Properties

| Property | Type | Description |
| --------- | ----------- |
| [`originalImageHashId`](#originalimagehashid) | *String* | The hash ID of the original image. You can use this ID to get the original image via the `IntermediateResultManager` class. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) |  *Matrix4* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`](#errorcode) | *int* | The error code associated with the capture result. |
| [`errorMessage`](#errormessage) | *String* | The error message associated with the capture result. |
| [`decodedBarcodesResult`](#decodedbarcodesresult) | [*DecodedBarcodesResult*]({{ site.dbr_flutter_api }}barcode-reader/decoded-barcodes-result.html) | A [`DecodedBarcodesResult`](decoded-barcodes-result.md) object that represents all of the decoded barcode(s) within the original image. |

### originalImageHashId

Returns the hash ID of the original image that contains the captured result. You can use this ID to get the original image via the [`IntermediateResultManager`](./intermediate-result-manager.md) class.

```dart
String originalImageHashId,
```

### rotationTransformMatrix

The rotation transformation matrix (represented as a [`Matrix4`](https://api.flutter.dev/flutter/package-vector_math_vector_math_64/Matrix4-class.html)]) of the original image relative to the rotated image.

```dart
Matrix4 rotationTransformMatrix;
```

### errorCode

The error code produced by the library and associated with the captured result should something go wrong during the recognition process.

```dart
int errorCode;
```

### errorMessage

The error string associated with the error code, providing details about the error.

```dart
String errorMessage;
```

### decodedBarcodesResult

A [`DecodedBarcodesResult`]({{ site.dbr_flutter_api }}barcode-reader/decoded-barcodes-result.html) object that represents all of the decoded barcode(s) within the original image.

```dart
DecodedBarcodesResult? decodedBarcodesResult;
```
