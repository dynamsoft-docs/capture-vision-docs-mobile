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

The `CapturedResultReceiver` interface provides methods for monitoring the output of captured results, which can consist of original image result(s), decoded barcode result(s), recognized text line result(s), detected quad result(s), normalized image result(s), or parsed result(s). The `CapturedResultReceiver` can add a receiver for any type of captured result or for a specific type of captured result, based on the method that is implemented.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
interface CapturedResultReceiver
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`onCapturedResultReceived`](#oncapturedresultreceived) | The method for monitoring the output of `CapturedResult`. |
| [`onOriginalImageResultReceived`](#onoriginalimageresultreceived) | The method for monitoring the output of `OriginalImageResultItem`. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The method for monitoring the output of `DecodedBarcodesResult`. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The method for monitoring the output of `RecognizedTextLinesResult`. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | The method for monitoring the output of `DetectedQuadsResult`. |
| [`onNormalizedImagesReceived`](#onnormalizedimagesreceived) | The method for monitoring the output of `NormalizedImagesResult`. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | The method for monitoring the output of `ParsedResult`. |

### onCapturedResultReceived

The method for monitoring the output of [`CapturedResult`](captured-result.md).

```java
void onCapturedResultReceived(CapturedResult result);
```

**Parameters**

`[in] result`: A [`CapturedResult`](captured-result.md) object as a captured result.

### onOriginalImageResultReceived

The method for monitoring the output of [`OriginalImageResultItem`](original-image-result-item.md).

```java
void onOriginalImageResultReceived(OriginalImageResultItem result);
```

**Parameters**

`[in] result`: A [`OriginalImageResultItem`](original-image-result-item.md) object as a original image result.

### onDecodedBarcodesReceived

The method for monitoring the output of `DecodedBarcodesResult`.

```java
void onDecodedBarcodesReceived(DecodedBarcodesResult result);
```

**Parameters**

`[in] result`: A `DecodedBarcodesResult` object as a decoded barcode result.

### onRecognizedTextLinesReceived

The method for monitoring the output of `RecognizedTextLinesResult`.

```java
void onRecognizedTextLinesReceived(RecognizedTextLinesResult result);
```

**Parameters**

`[in] result`: A `RecognizedTextLinesResult` object as a recognized text line result.

### onDetectedQuadsReceived

The method for monitoring the output of [`DetectedQuadsResult`]({{site.android_api}}detected-quads-result.html).

```java
void onDetectedQuadsReceived(DetectedQuadsResult result);
```

**Parameters**

`[in] result`: A [`DetectedQuadsResult`]({{site.android_api}}detected-quads-result.html) object as a detected quad result.

### onNormalizedImagesReceived

The method for monitoring the output of [`NormalizedImagesResult`]({{site.android_api}}normalized-images-result.html).

```java
void onNormalizedImagesReceived(NormalizedImagesResult result);
```

**Parameters**

`[in] result`: A [`NormalizedImagesResult`]({{site.android_api}}normalized-images-result.html) object as a normalized image result.

### onParsedResultsReceived

The method for monitoring the output of `ParsedResult`.

```java
void onParsedResultsReceived(ParsedResult result);
```

**Parameters**

`[in] result`: A `ParsedResult` object as a parsed result.
