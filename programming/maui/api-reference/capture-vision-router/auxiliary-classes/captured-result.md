---
layout: default-layout
title: CapturedResult Class - Dynamsoft Capture Vision MAUI Edition
description: CapturedResult class of DCV MAUI edition represents the result of a capture operation on an image.
keywords: decoded barcode, parsed result, error code, output, captured result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResult

The `CapturedResult` class represents the result of a capture operation on an image. Internally, `CapturedResult` stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, original image, parsed item, etc.

> You might also looking for:
>
> - [DecodedBarcodesResult]({{ site.dbr_maui_api }}decoded-barcodes-result.html)
> - [ParsedResults]({{ site.dcp_maui_api }}parsed-result.html)

## Definition

*Namespace:* Dynamsoft.CaptureVisionRouter.Maui

*Assembly:* Dynamsoft.CaptureVisionRouter.Maui

```csharp
class CapturedResult : CapturedResultBase
```

## Properties

| Property | Description |
| --------- | ----------- |
| [`DecodedBarcodesResult`](#decodedbarcodesresult) | A [`DecodedBarcodesResult`]({{ site.dbr_maui_api }}decoded-barcodes-result.html) object that represents all decoded barcode. |
| [`ParsedResult`](#parsedresult) | A [`ParsedResult`]({{ site.dcp_maui_api }}parsed-result.html) that represents all parsed result items. |
| [`RecognizedTextLinesResult`](#recognizedtextlinesresult) | A [`RecognizedTextLinesResult`]({{ site.dtr_maui_api }}recognized-text-lines-result.html) object that represents all recognized text lines. |
| [`ProcessedDocumentResult`](#processeddocumentresult) | A [`ProcessedDocumentResult`]({{ site.ddn_maui_api }}processed-document-result.html) objects, that represents all the detected quads, deskewed images or enhanced images. |

The following properties are inherited from [`CapturedResultBase`]({{ site.dcv_maui_api }}core/captured-result-base.html):

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`OriginalImageHashId`]({{ site.dcv_maui_api }}core/captured-result-base.html#originalimagehashid) | *string* | Represents the hash id of the original image. |
| [`RotationTransformMatrix`]({{ site.dcv_maui_api }}core/captured-result-base.html#rotationtransformmatrix) | *Matrix* | Represents the rotation transformation matrix of the original image relative to the rotated image. |
| [`ErrorCode`]({{ site.dcv_maui_api }}core/captured-result-base.html#errorcode) | *int* | Represents the error code of this result. |
| [`ErrorMessage`]({{ site.dcv_maui_api }}core/captured-result-base.html#errormessage) | *string* | Represents the error message of this result. |

### DecodedBarcodesResult

A [`DecodedBarcodesResult`]({{ site.dbr_maui_api }}decoded-barcodes-result.html) object that represents all decoded barcode within the original image.

```csharp
DecodedBarcodesResult DecodedBarcodesResult { get; }
```

### ParsedResult

A [`ParsedResult`]({{ site.dcp_maui_api }}parsed-result.html) that represents all parsed result items within the original image.

```csharp
ParsedResult ParsedResult { get; }
```

### RecognizedTextLinesResult

A [`RecognizedTextLinesResult`]({{ site.dtr_maui_api }}recognized-text-lines-result.html) object that represents all recognized text lines within the original image.

```csharp
RecognizedTextLinesResult RecognizedTextLinesResult { get; }
```

### ProcessedDocumentResult

A [`ProcessedDocumentResult`]({{ site.ddn_maui_api }}processed-document-result.html) objects, that represents all the detected quads, deskewed images or enhanced images.

```csharp
ProcessedDocumentResult ProcessedDocumentResult { get; }
```
