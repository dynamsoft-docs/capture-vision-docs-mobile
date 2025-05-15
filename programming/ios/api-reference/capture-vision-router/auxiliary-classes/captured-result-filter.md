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
| [`onProcessedDocumentResultReceived`](#onprocesseddocumentresultreceived) | The method for monitoring the output of `ProcessedDocumentResult`, which includes the detected quad, deskewed image and enhanced image. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | The method for monitoring the output of `DSParsedResult`. |

### onOriginalImageResultReceived

The method for monitoring the output of [`DSOriginalImageResultItem`]({{ site.dcv_ios_api }}core/basic-structures/original-image-result-item.html).

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

The method for monitoring the output of [DSDecodedBarcodesResult]({{ site.dbr_ios_api }}decoded-barcodes-result.html).

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

The method for monitoring the output of [DSRecognizedTextLinesResult]({{ site.dlr_ios_api }}recognized-text-lines-result.html).

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

### onProcessedDocumentResultReceived

The method for monitoring the output of [DSProcessedDocumentResult]({{site.ddn_ios_api}}processed-document-result.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onProcessedDocumentResultReceived:(DSProcessedDocumentResult*)result;
```
2. 
```swift
func onProcessedDocumentResultReceived(_ result: ProcessedDocumentResult)
```

**Parameters**

`result`: A [`DSProcessedDocumentResult`]({{site.ddn_ios_api}}processed-document-result.html) object as a processed document result.

### onParsedResultsReceived

The method for monitoring the output of [DSParsedResult]({{ site.dcp_ios_api }}parsed-result.html).

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
