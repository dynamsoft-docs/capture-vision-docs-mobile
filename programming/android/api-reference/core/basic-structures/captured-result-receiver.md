---
layout: default-layout
Title: CapturedResultReceiver - Dynamsoft Core Module Android Edition API Reference
Description: The interface CapturedResultReceiver of Dynamsoft Core Module Android Edition provides methods for monitoring the output of captured results, including captured result, raw image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, and parsed result.
Keywords: captured result, raw image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, parsed result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultReceiver

The `CapturedResultReceiver` interface provides methods for monitoring the output of captured results, including captured result, raw image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, and parsed result.

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
| [`onRawImageResultReceived`](#onrawimageresultreceived) | The method for monitoring the output of `RawImageResultItem`. |
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

### onRawImageResultReceived

The method for monitoring the output of [`RawImageResultItem`](raw-image-result-item.md).

```java
void onRawImageResultReceived(RawImageResultItem result);
```

**Parameters**

`[in] result`: A [`RawImageResultItem`](raw-image-result-item.md) object as a raw image result.

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
