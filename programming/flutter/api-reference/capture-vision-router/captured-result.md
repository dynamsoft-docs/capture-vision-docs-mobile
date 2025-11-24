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
class CapturedResult extends CapturedResultBase
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`items`](#items) | *List\<CapturedResultItem\>?* | A list of [`CapturedResultItem`](captured-result-item.md) objects. |
| [`decodedBarcodesResult`](#decodedbarcodesresult) | [*DecodedBarcodesResult*]({{ site.dbr_flutter_api }}barcode-reader/decoded-barcodes-result.html) | All results of type `barcode` in the `CapturedResult` as a `DecodedBarcodesResult` object. |
| [`recognizedTextLinesResult`](#recognizedtextlinesresult) | [*RecognizedTextLinesResult*]({{ site.dlr_flutter_api }}recognized-text-lines-result.html) | All results of type `textLine` in the `CapturedResult` as a `RecognizedTextLinesResult` object. |
| [`processedDocumentResult`](#processeddocumentresult) | [*ProcessedDocumentResult*]({{ site.ddn_flutter_api }}processed-document-result.html) | All results of type `detectedQuad`, `deskewedImage` and `enhancedImage` in the `CapturedResult` as a `ProcessedDocumentResult` object. |
| [`parsedResult`](#parsedresult) | [*ParsedResult*]({{ site.dcp_flutter_api }}parsed-result.html) | All results of type `parsedResult` in the `CapturedResult` as a `ParsedResult` object. |


### items

A list of [`CapturedResultItem`]({{ site.crr_flutter_api }}captured-result-item.html) objects.

```dart
List<CapturedResultItem>? items;
```

### decodedBarcodesResult

All results of type `barcode` in the `CapturedResult` as a `DecodedBarcodesResult` object.

```dart
DecodedBarcodesResult? decodedBarcodesResult;
```

### recognizedTextLinesResult

All results of type `textLine` in the `CapturedResult` as a `RecognizedTextLinesResult` object.

```dart
RecognizedTextLinesResult? recognizedTextLinesResult;
```

#### processedDocumentResult

All results of type `detectedQuad`, `deskewedImage` and `enhancedImage` in the `CapturedResult` as a `ProcessedDocumentResult` object.

```dart
ProcessedDocumentResult? processedDocumentResult;
```

### parsedResult

All results of type `parsedResult` in the `CapturedResult` as a `ParsedResult` object.

```dart
ParsedResult? parsedResult;
```
