---
layout: default-layout
title: CapturedResultFilter - Dynamsoft Core Module Android Edition API Reference
description: The interface CapturedResultFilter of Dynamsoft Core Module represents a captured result filter, which is responsible for filtering different types of captured results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.
keywords: captured result filter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultFilter

The `CapturedResultFilter` interface represents a captured result filter, which is responsible for filtering different types of captured results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
interface CapturedResultFilter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`onOriginalImageResultReceived`](#onoriginalimageresultreceived) | The method for monitoring the output of `OriginalImageResultItem`. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The method for monitoring the output of `DecodedBarcodesResult`. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The method for monitoring the output of `RecognizedTextLinesResult`. |
| [`onProcessedDocumentResultReceived`](#onprocesseddocumentresultreceived) | The method for monitoring the output of `ProcessedDocumentResult`, which includes the detected quad, deskewed image and enhanced image. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | The method for monitoring the output of `ParsedResult`. |

### onOriginalImageResultReceived

The method for monitoring the output of [`OriginalImageResultItem`]({{ site.dcv_android_api }}core/basic-structures/original-image-result-item.html).

```java
void onOriginalImageResultReceived(OriginalImageResultItem result);
```

**Parameters**

`[in] result`: A [`OriginalImageResultItem`]({{ site.dcv_android_api }}core/basic-structures/original-image-result-item.html) object as a original image result.

### onDecodedBarcodesReceived

The method for monitoring the output of DecodedBarcodesResult.

```java
void onDecodedBarcodesReceived(DecodedBarcodesResult result);
```

**Parameters**

`[in] result`: A `DecodedBarcodesResult` object as a decoded barcode result.

### onRecognizedTextLinesReceived

The method for monitoring the output of RecognizedTextLinesResult.

```java
void onRecognizedTextLinesReceived(RecognizedTextLinesResult result);
```

**Parameters**

`[in] result`: A `RecognizedTextLinesResult` object as a recognized text line result.

### onProcessedDocumentResultReceived

The method for monitoring the output of `ProcessedDocumentResult`, which includes the detected quad, deskewed image and enhanced image.

```java
void onProcessedDocumentResultReceived(ProcessedDocumentResult result);
```

**Parameters**

`[in] result`: A `ProcessedDocumentResult` object as a processed document result.

### onParsedResultsReceived

The method for monitoring the output of ParsedResult.

```java
void onParsedResultsReceived(ParsedResult result);
```

**Parameters**

`[in] result`: A `ParsedResult` object as a parsed result.
