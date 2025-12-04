---
layout: default-layout
title: CapturedResultBase - Dynamsoft Capture Vision Flutter
description: The class CapturedResultBase of Dynamsoft Core Module Flutter edition is the base class of all types of captured results.
keywords: captured result base, Flutter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultBase

The `CapturedResultBase` class is the base class of all types of captured results.

> [!NOTE]
> Sub classes:
> - Barcode: [`DecodedBarcodesResult`]({{ site.dbr_flutter_api }}barcode-reader/decoded-barcodes-result.html)
> - Text line: [`RecognizedTextLinesResult`]({{ site.dlr_flutter_api }}recognized-text-lines-result.html)
> - Document page(s): [`ProcessedDocumentResult`]({{ site.ddn_flutter_api }}processed-document-result.html)
> - Parsed content (DL, MRZ, VIN, GS1 AI, etc.): [`ParsedResult`]({{ site.dcp_flutter_api }}parsed-result.html)

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class CapturedResultBase
```

## Properties

| Properties | Types | Description |
| ---------- | ----- | ----------- |
| [`originalImageHashId`](#originalimagehashid) | *String* | The hash id of the original image. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *Matrix4* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`](#errorcode) | *int* | The error code of this result. |
| [`errorMessage`](#errormessage) | *String* | The error message of this result. |

### originalImageHashId

The hash id of the original image.

```dart
String originalImageHashId;
```

### rotationTransformMatrix

The rotation transformation matrix of the original image relative to the rotated image.

```dart
Matrix4 rotationTransformMatrix;
```

### errorCode

The error code of this result.

```dart
int errorCode;
```

### errorMessage

The error message of this result.

```dart
String? errorMessage;
```
