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
class CapturedResult
```

## Properties

| Property | Description |
| --------- | ----------- |
| [`OriginalImageHashId`](#originalimagehashid) | The hash id of the original image. You can use this ID to get the original image via the `IntermediateResultManager` class. |
| [`RotationTransformMatrix`](#rotationtransformmatrix) | The rotation transformation matrix of the original image relative to the rotated image. |
| [`ErrorCode`](#errorcode) | The error code associated with the capture result. |
| [`ErrorMessage`](#errormessage) | The error message associated with the capture result. |
| [`DecodedBarcodesResult`](#decodedbarcodesresult) | An array of `BarcodeResultItem` objects, each representing a decoded barcode within the original image. |
| [`ParsedResult`](#parsedresult) | An array of `ParsedResultItem` objects. |

### OriginalImageHashId

The hash id of the original image. You can use this ID to get the original image via the [`IntermediateResultManager`]({{ site.dcv_maui_api }}capture-vision-router/auxiliary-classes/intermediate-result-manager.html) class.

```csharp
string OriginalImageHashId { get;}
```

### RotationTransformMatrix

The rotation transformation matrix of the original image relative to the rotated image.

```csharp
Matrix RotationTransformMatrix { get; }
```

### ErrorCode

Error code associated with the capture result.

```csharp
int ErrorCode { get; }
```

### ErrorMessage

Error string providing details about the error.

```csharp
string ErrorMessage { get; }
```

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
