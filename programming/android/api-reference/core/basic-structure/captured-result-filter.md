---
layout: default-layout
Title: CapturedResultFilter - Dynamsoft Core Module Android Edition API Reference
Description: The protocol CapturedResultFilter of Dynamsoft Core Module represents a captured result filter, which is responsible for filtering different types of captured results, including raw image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.
Keywords: captured result filter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultFilter

The `CapturedResultFilter` protocol represents a captured result filter, which is responsible for filtering different types of captured results, including raw image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Declaration

```java
interface CapturedResultFilter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`onRawImageResultReceived`](#onrawimageresultreceived) | The method for monitoring the output of `DSRawImageResultItem`. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The method for monitoring the output of `DSDecodedBarcodesResult`. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The method for monitoring the output of `DSRecognizedTextLinesResult`. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | The method for monitoring the output of `DSDetectedQuadsResult`. |
| [`onNormalizedImagesReceived`](#onnormalizedimagesreceived) | The method for monitoring the output of `DSNormalizedImagesResult`. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | The method for monitoring the output of `DSParsedResult`. |

### onRawImageResultReceived

The method for monitoring the output of DSRawImageResultItem.

```java
func onRawImageResultReceived(_ result: DSRawImageResultItem)
```

**Parameters**

`result`: A `DSRawImageResultItem` object as a raw image result.

### onDecodedBarcodesReceived

The method for monitoring the output of DSDecodedBarcodesResult.

```java
func onDecodedBarcodesReceived(_ result: DSDecodedBarcodesResult)
```

**Parameters**

`result`: A `DSDecodedBarcodesResult` object as a decoded barcode result.

### onRecognizedTextLinesReceived

The method for monitoring the output of DSRecognizedTextLinesResult.

```java
func onRecognizedTextLinesReceived(_ result: DSRecognizedTextLinesResult)
```

**Parameters**

`result`: A `DSRecognizedTextLinesResult` object as a recognized text line result.

### onDetectedQuadsReceived

The method for monitoring the output of DSDetectedQuadsResult.

```java
func onDetectedQuadsReceived(_ result: DSDetectedQuadsResult)
```

**Parameters**

`result`: A `DSDetectedQuadsResult` object as a detected quad result.

### onNormalizedImagesReceived

The method for monitoring the output of DSNormalizedImagesResult.

```java
func onNormalizedImagesReceived(_ result: DSNormalizedImagesResult)
```

**Parameters**

`result`: A `DSNormalizedImagesResult` object as a normalized image result.

### onParsedResultsReceived

The method for monitoring the output of DSParsedResult.

```java
func onParsedResultsReceived(_ result: DSParsedResult)
```

**Parameters**

`result`: A `DSParsedResult` object as a parsed result.
