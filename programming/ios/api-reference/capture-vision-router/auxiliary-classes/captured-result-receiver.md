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

The `DSCapturedResultReceiver` interface is designed as a standardized way for retrieving captured results in the Dynamsoft Capture Vision architecture. By implementing the `DSCapturedResultReceiver`, you will receive the callback of the various types of captured results, such as original image, decoded barcode, recognized text line, detected quad, normalized image, or parsed data. The `DSCapturedResultReceiver` can add a receiver for any type of captured result or for a specific type of captured result, based on the method that is implemented.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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
| [`onCapturedResultReceived`](#oncapturedresultreceived) | The callback triggered when a generic captured result is available, occurring each time an image finishes its processing. |
| [`onOriginalImageResultReceived`](#onoriginalimageresultreceived) | The callback triggered when the original image result is available, occurring each time an image finishes its processing. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The callback triggered when decoded barcodes are available, occurring each time an image finishes its processing. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The callback triggered when recognized text lines are available, occurring each time an image finishes its processing. |
| [`onProcessedDocumentResultReceived`](#onprocesseddocumentresultreceived) | The callback triggered when processed document results are available, occurring each time an image finishes its processing. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | The callback triggered when parsed results are available, occurring each time an image finishes its processing. |

### onCapturedResultReceived

The callback method triggered when a generic captured result is available, occurring each time an image finishes its processing. This callback can be used for any result that does not fit into the specific categories of the other callbacks.

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

The callback method triggered when the original image result is available, occurring each time an image finishes its processing. This callback is used to handle the original image that used as the input of this capture process.

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

`result` : A [`DSOriginalImageResultItem`]({{ site.dcv_ios_api }}core/basic-structures/original-image-result-item.html) object as a original image result.

### onDecodedBarcodesReceived

The callback triggered when decoded barcodes are available, occurring each time an image finishes its processing.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onDecodedBarcodesReceived:(DSDecodedBarcodesResult*)result;
```
1. 
```swift
func onDecodedBarcodesReceived(_ result: DSDecodedBarcodesResult)
```

**Parameters**

`result` : A [`DSDecodedBarcodesResult`]({{site.dbr_ios_api}}decoded-barcodes-result.html}}) object as a decoded barcode result.

### onRecognizedTextLinesReceived

The callback triggered when recognized text lines are available, occurring each time an image finishes its processing.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onRecognizedTextLinesReceived:(DSRecognizedTextLinesResult*)result;
```
1. 
```swift
func onRecognizedTextLinesReceived(_ result: DSRecognizedTextLinesResult)
```

**Parameters**

`result` : A [`DSRecognizedTextLinesResult`]({{site.dlr_ios_api}}recognized-text-lines-result.html) object as a recognized text line result.

### onProcessedDocumentResultReceived

The callback triggered when processed document results are available, occurring each time an image finishes its processing.

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

The callback triggered when parsed results are available, occurring each time an image finishes its processing.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onParsedResultsReceived:(DSParsedResult*)result;
```
1. 
```swift
func onParsedResultsReceived(_ result: DSParsedResult)
```

**Parameters**

`result` : A [`DSParsedResult`]({{site.dcp_ios_api}}parsed-result.html) object as a parsed result.
