---
layout: default-layout
title: CapturedResultReceiver - Dynamsoft Core Module Android Edition API Reference
description: The interface CapturedResultReceiver of Dynamsoft Core Module Android Edition provides methods for monitoring the output of captured results, including captured result, original image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, and parsed result.
keywords: captured result, original image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, parsed result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultReceiver

The `CapturedResultReceiver` interface is designed as a standardized way for retrieving captured results in the Dynamsoft Capture Vision architecture. By implementing the `CapturedResultReceiver`, you will receive the callback of the various types of captured results, such as original image, decoded barcode, recognized text line, detected quad, normalized image, or parsed data. The `CapturedResultReceiver` can add a receiver for any type of captured result or for a specific type of captured result, based on the method that is implemented.

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionRouter.aar

```java
interface CapturedResultReceiver
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`onCapturedResultReceived`](#oncapturedresultreceived) | The callback triggered when a generic captured result is available, occurring each time an image finishes its processing. |
| [`onOriginalImageResultReceived`](#onoriginalimageresultreceived) | The callback triggered when the original image result is available, occurring each time an image finishes its processing. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The callback triggered when decoded barcodes are available, occurring each time an image finishes its processing. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The callback triggered when recognized text lines are available, occurring each time an image finishes its processing. |
| [`onProcessedDocumentResultReceived`](#onprocesseddocumentresultreceived) | The callback triggered when processed document results are available, occurring each time an image finishes its processing. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | The callback triggered when parsed results are available, occurring each time an image finishes its processing. |

### onCapturedResultReceived

The callback method triggered when a generic captured result is available, occurring each time an image finishes its processing. This callback can be used for any result that does not fit into the specific categories of the other callbacks.

```java
void onCapturedResultReceived(CapturedResult result);
```

**Parameters**

`[in] result`: The captured result, an instance of [`CapturedResult`](captured-result.md).

### onOriginalImageResultReceived

The callback method triggered when the original image result is available, occurring each time an image finishes its processing. This callback is used to handle the original image that used as the input of this capture process.

```java
void onOriginalImageResultReceived(OriginalImageResultItem result);
```

**Parameters**

`[in] result`: The original image result, an instance of [`OriginalImageResultItem`]({{ site.dcv_android_api }}core/basic-structures/original-image-result-item.html).

### onDecodedBarcodesReceived

The callback triggered when decoded barcodes are available, occurring each time an image finishes its processing.

```java
void onDecodedBarcodesReceived(DecodedBarcodesResult result);
```

**Parameters**

`[in] result`: The decoded barcode result, an instance of `DecodedBarcodesResult`.

### onRecognizedTextLinesReceived

The callback triggered when recognized text lines are available, occurring each time an image finishes its processing.

```java
void onRecognizedTextLinesReceived(RecognizedTextLinesResult result);
```

**Parameters**

`[in] result`: The recognized text lines result, an instance of [`RecognizedTextLinesResult`]({{site.dlr_android_api}}recognized-text-lines-result.html).

### onProcessedDocumentResultReceived

The callback triggered when processed document results are available, occurring each time an image finishes its processing.

```java
void onProcessedDocumentResultReceived(ProcessedDocumentResult result);
```

**Parameters**

`[in] result`: A [`ProcessedDocumentResult`]({{site.ddn_android_api}}processed-document-result.html) object as a processed document result.

### onParsedResultsReceived

The callback triggered when parsed results are available, occurring each time an image finishes its processing.

```java
void onParsedResultsReceived(ParsedResult result);
```

**Parameters**

`[in] result`: The parsed result, an instance of [`ParsedResult`]({{site.dcp_android_api}}parsed-result.html).
