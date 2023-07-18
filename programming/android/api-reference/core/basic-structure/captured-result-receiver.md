---
layout: default-layout
Title: CapturedResultReceiver - Dynamsoft Core Module Android Edition API Reference
Description: The protocol CapturedResultReceiver of Dynamsoft Core Module Android Edition provides methods for monitoring the output of captured results, including captured result, raw image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, and parsed result.
Keywords: captured result, raw image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, parsed result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultReceiver

The `CapturedResultReceiver` protocol provides methods for monitoring the output of captured results, including captured result, raw image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, and parsed result.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
interface CapturedResultReceiver
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`onCapturedResultReceived`](#oncapturedresultreceived) | The method for monitoring the output of `CapturedResult`. |
| [`onRawImageResultReceived`](#onrawimageresultreceived) | The method for monitoring the output of `DSRawImageResultItem`. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The method for monitoring the output of `DSDecodedBarcodesResult`. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The method for monitoring the output of `DSRecognizedTextLinesResult`. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | The method for monitoring the output of `DSDetectedQuadsResult`. |
| [`onNormalizedImagesReceived`](#onnormalizedimagesreceived) | The method for monitoring the output of `DSNormalizedImagesResult`. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | The method for monitoring the output of `DSParsedResult`. |

### onCapturedResultReceived

The method for monitoring the output of `CapturedResult`.

```java
func onCapturedResultReceived(_ result: CapturedResult)
```

**Parameters**

`result`: A `CapturedResult` object as a captured result.

### onRawImageResultReceived

The method for monitoring the output of `DSRawImageResultItem`.

```java
func onRawImageResultReceived(_ result: DSRawImageResultItem)
```

**Parameters**

`result`: A `DSRawImageResultItem` object as a raw image result.

### onDecodedBarcodesReceived

The method for monitoring the output of `DSDecodedBarcodesResult`.

```java
func onDecodedBarcodesReceived(_ result: DSDecodedBarcodesResult)
```

**Parameters**

`result`: A `DSDecodedBarcodesResult` object as a decoded barcode result.

### onRecognizedTextLinesReceived

The method for monitoring the output of `DSRecognizedTextLinesResult`.

```java
func onRecognizedTextLinesReceived(_ result: DSRecognizedTextLinesResult)
```

**Parameters**

`result`: A `DSRecognizedTextLinesResult` object as a recognized text line result.

### onDetectedQuadsReceived

The method for monitoring the output of `DSDetectedQuadsResult`.

```java
func onDetectedQuadsReceived(_ result: DSDetectedQuadsResult)
```

**Parameters**

`result`: A `DSDetectedQuadsResult` object as a detected quad result.

### onNormalizedImagesReceived

The method for monitoring the output of `DSNormalizedImagesResult`.

```java
func onNormalizedImagesReceived(_ result: DSNormalizedImagesResult)
```

**Parameters**

`result`: A `DSNormalizedImagesResult` object as a normalized image result.

### onParsedResultsReceived

The method for monitoring the output of `DSParsedResult`.

```java
func onParsedResultsReceived(_ result: DSParsedResult)
```

**Parameters**

`result`: A `DSParsedResult` object as a parsed result.
