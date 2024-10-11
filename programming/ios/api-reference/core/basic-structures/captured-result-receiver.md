---
layout: default-layout
title: DSCapturedResultReceiver - Dynamsoft Core Module iOS Edition API Reference
description: The protocol DSCapturedResultReceiver of Dynamsoft Core Module iOS Edition provides methods for monitoring the output of captured results, including captured result, original image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, and parsed result.
keywords: captured result, original image result, decoded barcode result, recognized text line result, detected quad result, normalized image result, parsed result, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# DSCapturedResultReceiver

The `DSCapturedResultReceiver` protocol provides methods for monitoring the output of captured results, which can consist of original image result(s), decoded barcode result(s), recognized text line result(s), detected quad result(s), normalized image result(s), or parsed result(s). The `DSCapturedResultReceiver` can add a receiver for any type of captured result or for a specific type of captured result, based on the method that is implemented.

## Definition

*Assembly:* DynamsoftCore.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@protocol DSCapturedResultReceiver <NSObject>
```
2. 
```swift
protocol CapturedResultReceiver: NSObjectProtocol
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`onCapturedResultReceived`](#oncapturedresultreceived) | The method for monitoring the output of `DSCapturedResult`. |
| [`onOriginalImageResultReceived`](#onoriginalimageresultreceived) | The method for monitoring the output of `DSOriginalImageResultItem`. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The method for monitoring the output of `DSDecodedBarcodesResult`. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The method for monitoring the output of `DSRecognizedTextLinesResult`. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | The method for monitoring the output of `DSDetectedQuadsResult`. |
| [`onNormalizedImagesReceived`](#onnormalizedimagesreceived) | The method for monitoring the output of `DSNormalizedImagesResult`. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | The method for monitoring the output of `DSParsedResult`. |

### onCapturedResultReceived

The method for monitoring the output of `DSCapturedResult`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onCapturedResultReceived:(DSCapturedResult*)result;
```
2. 
```swift
func onCapturedResultReceived(_ result: DSCapturedResult)
```

**Parameters**

`result` : A [`DSCapturedResult`](captured-result.md) object as a captured result.

### onOriginalImageResultReceived

The method for monitoring the output of `DSOriginalImageResultItem`.

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

`result` : A [`DSOriginalImageResultItem`](original-image-result-item.md) object as a original image result.

### onDecodedBarcodesReceived

The method for monitoring the output of `DSDecodedBarcodesResult`.

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

`result` : A `DSDecodedBarcodesResult` object as a decoded barcode result.

### onRecognizedTextLinesReceived

The method for monitoring the output of `DSRecognizedTextLinesResult`.

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

`result` : A `DSRecognizedTextLinesResult` object as a recognized text line result.

### onDetectedQuadsReceived

The method for monitoring the output of `DSDetectedQuadsResult`.

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

`result` : A [`DSDetectedQuadsResult`](quadrilateral.md) object as a detected quad result.

### onNormalizedImagesReceived

The method for monitoring the output of `DSNormalizedImagesResult`.

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

`result` : A `DSNormalizedImagesResult` object as a normalized image result.

### onParsedResultsReceived

The method for monitoring the output of `DSParsedResult`.

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

`result` : A `DSParsedResult` object as a parsed result.
