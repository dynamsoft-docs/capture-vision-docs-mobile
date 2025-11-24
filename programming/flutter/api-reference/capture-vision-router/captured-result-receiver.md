---
layout: default-layout
title: CapturedResultReceiver Interface - Dynamsoft Capture Vision Flutter
description: CapturedResultReceiver interface of DCV Flutter edition is designed as a standardized way for retrieving captured results.
keywords: decoded barcodes, parsed results, captured results, CRR, result receiver, output, flutter, barcode reader
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultReceiver

The `CapturedResultReceiver` interface is designed as a standardized way for retrieving captured results in the Dynamsoft Capture Vision architecture. By implementing the `CapturedResultReceiver`, you will receive the callback of the various types of *captured results*, such a decoded barcode (Barcode Reader), a recognized text line (Label Recognizer), a detected quad (Document Normalizer), a normalized image (Document Normalizer), or parsed data (Code Parser). The `CapturedResultReceiver` can add a receiver for any type of captured result or for a specific type of captured result, based on the method that is implemented.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class CapturedResultReceiver
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`onCapturedResultReceived`](#oncapturedresultreceived) | The callback invoked when captured results become available. It is triggered once for each image after its processing is completed. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The callback invoked when decoded barcodes become available. It is triggered once for each image after its processing is completed. |
| [`onParsedResultsReceived`](#onparsedreultsreceived) | The callback invoked when parsed results become available. It is triggered once for each image after its processing is completed.|
| [`onProcessedDocumentResultReceived`](#onparsedreultsreceived) | The callback invoked when processed document results become available. It is triggered once for each image after its processing is completed. |
| [`onRecognizedTextLinesReceived`](#onparsedreultsreceived) | The callback invoked when recognized text lines become available. It is triggered once for each image after its processing is completed. |

### onCapturedResultReceived

This callback method delivers a [`CapturedResult`](captured-result.md) - an object representing any kind of captured result item that is captured from an image or a video frame. The callback is triggered each time an image finishes processing, regardless of whether there is a valid result or not.

```dart
Future<void> Function(CapturedResult result)? onCapturedResultReceived;
```

**Parameters**

`result`: The captured result, an instance of [`CapturedResult`](captured-result.md).

### onDecodedBarcodesReceived

This callback method delivers a [`DecodedBarcodesResult`]({{ site.dbr_flutter_api }}barcode-reader/decoded-barcodes-result.html), which is an object representing any captured result of type `barcode` that is taken from an image or a video frame. The callback is triggered each time an image finishes processing, regardless of whether there is a valid result or not.

```dart
Future<void> Function(DecodedBarcodesResult result)? onDecodedBarcodesReceived;
```

**Parameters**

`result`: The decoded barcode result, an instance of [`DecodedBarcodesResult`]({{ site.dbr_flutter_api }}barcode-reader/decoded-barcodes-result.html).

### onParsedReultsReceived

This callback method delivers a [`ParsedResult`]({{ site.dcp_flutter_api }}parsed-result.html), which is an object representing any captured result of type `parsedResult` that is taken from an image or a video frame. The callback is triggered each time an image finishes processing, regardless of whether there is a valid result or not.

```dart
Future<void> Function(ParsedResult result)? onParsedResultsReceived;
```

**Parameters**

`result`: The parsed result, an instance of [`ParsedResult`]({{ site.dcp_flutter_api }}parsed-result.html).

### onProcessedDocumentResultReceived

This callback method delivers a [`ProcessedDocumentResult`]({{ site.ddn_flutter_api }}processed-document-result.html), which is an object representing any captured result of type `detectedQuad`, `deskewedImage` and `enhancedImage` that is taken from an image or a video frame. The callback is triggered each time an image finishes processing, regardless of whether there is a valid result or not.

```dart
Future<void> Function(ProcessedDocumentResult result)? onProcessedDocumentResultReceived;
```

**Parameters**

`result`: The document processing results, an instance of [`ProcessedDocumentResult`]({{ site.ddn_flutter_api }}processed-document-result.html).

### onRecognizedTextLinesReceived

This callback method delivers a [`RecognizedTextLinesResult`]({{ site.dlr_flutter_api }}recognized-text-lines-result.html), which is an object representing any captured result of type `recognizedTextLines` that is taken from an image or a video frame. The callback is triggered each time an image finishes processing, regardless of whether there is a valid result or not.

```dart
Future<void> Function(RecognizedTextLinesResult result)? onRecognizedTextLinesReceived;
```

**Parameters**

`result`: The text recognition result, an instance of [`RecognizedTextLinesResult`]({{ site.dlr_flutter_api }}recognized-text-lines-result.html).
