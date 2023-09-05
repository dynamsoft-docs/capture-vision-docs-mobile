---
layout: default-layout
title: DSCapturedResultFilter - Dynamsoft Core Module iOS Edition API Reference
description: The protocol DSCapturedResultFilter of Dynamsoft Core Module represents a captured result filter, which is responsible for filtering different types of captured results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.
keywords: captured result filter, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCapturedResultFilter

The `DSCapturedResultFilter` protocol represents a captured result filter, which is responsible for filtering different types of captured results, including original image, decoded barcodes, recognized text lines, detected quads, normalized images, and parsed results.

## Declaration

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@protocol DSCapturedResultFilter : NSObject
```
2. 
```swift
protocol CapturedResultFilter : NSObjectProtocol
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`onOriginalImageResultReceived`](#onoriginalimageresultreceived) | The method for monitoring the output of `DSOriginalImageResultItem`. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The method for monitoring the output of `DSDecodedBarcodesResult`. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The method for monitoring the output of `DSRecognizedTextLinesResult`. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | The method for monitoring the output of `DSDetectedQuadsResult`. |
| [`onNormalizedImagesReceived`](#onnormalizedimagesreceived) | The method for monitoring the output of `DSNormalizedImagesResult`. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | The method for monitoring the output of `DSParsedResult`. |

### onOriginalImageResultReceived

The method for monitoring the output of DSOriginalImageResultItem.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onOriginalImageResultReceived:(DSOriginalImageResultItem*)result;
```
2. 
```swift
func onOriginalImageResultReceived(_ result: DSOriginalImageResultItem)
```

**Parameters**

`result`: A `DSOriginalImageResultItem` object as a original image result.

### onDecodedBarcodesReceived

The method for monitoring the output of DSDecodedBarcodesResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onDecodedBarcodesReceived:(DSDecodedBarcodesResult*)result;
```
2. 
```swift
func onDecodedBarcodesReceived(_ result: DSDecodedBarcodesResult)
```

**Parameters**

`result`: A `DSDecodedBarcodesResult` object as a decoded barcode result.

### onRecognizedTextLinesReceived

The method for monitoring the output of DSRecognizedTextLinesResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onRecognizedTextLinesReceived:(DSRecognizedTextLinesResult*)result;
```
2. 
```swift
func onRecognizedTextLinesReceived(_ result: DSRecognizedTextLinesResult)
```

**Parameters**

`result`: A `DSRecognizedTextLinesResult` object as a recognized text line result.

### onDetectedQuadsReceived

The method for monitoring the output of DSDetectedQuadsResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onDetectedQuadsReceived:(DSDetectedQuadsResult*)result;
```
2. 
```swift
func onDetectedQuadsReceived(_ result: DSDetectedQuadsResult)
```

**Parameters**

`result`: A `DSDetectedQuadsResult` object as a detected quad result.

### onNormalizedImagesReceived

The method for monitoring the output of DSNormalizedImagesResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onNormalizedImagesReceived:(DSNormalizedImagesResult*)result;
```
2. 
```swift
func onNormalizedImagesReceived(_ result: DSNormalizedImagesResult)
```

**Parameters**

`result`: A `DSNormalizedImagesResult` object as a normalized image result.

### onParsedResultsReceived

The method for monitoring the output of DSParsedResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onParsedResultsReceived:(DSParsedResult*)result;
```
2. 
```swift
func onParsedResultsReceived(_ result: DSParsedResult)
```

**Parameters**

`result`: A `DSParsedResult` object as a parsed result.
