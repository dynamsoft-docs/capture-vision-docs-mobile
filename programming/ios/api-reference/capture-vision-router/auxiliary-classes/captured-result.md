---
layout: default-layout
title: DSCapturedResult - Dynamsoft Capture Vision Module iOS Edition API Reference
description: The class DSCapturedResult of Dynamsoft Capture Vision Module represents the result of a capture operation on an image, which contains multiple items such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.
keywords: captured result, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCapturedResult

The `DSCapturedResult` class represents the result of a capture operation on an image. Internally, `DSCapturedResult` stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, original image, parsed item, etc.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCapturedResult : NSObject
```
2. 
```swift
class CapturedResult : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`originalImageHashId`](#originalimagehashid) | *NSString \** | The hash id of the original image. You can use this ID to get the original image via `IntermediateResultManager` class. |
| [`originalImageTag`](#originalimagetag) | *DSImageTag* | The [ImageTag]({{ site.dcv_ios_api }}core/basic-structures/image-tag.html) associated with the original image. |
| [`items`](#items) | *NSArray<DSCapturedResultItem*> \** | An array of `DSCapturedResultItems`, which are the basic item of the captured results. A `DSCapturedResultItem` can be an original image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View DSCapturedResultItemType for all available types. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`](#errorcode) | *NSInteger* | Error code associated with the capture result. |
| [`errorMessage`](#errormessage) | *NSString \** | Error message providing details about the error. |
| [`decodedBarcodesResult`](#decodedbarcodesresult) | *DSDecodedBarcodesResult* | A [`DSDecodedBarcodesResult`]({{ site.dbr_ios_api }}decoded-barcodes-result.html) object that contains all the [`DSBarcodesResultItems`]({{ site.dbr_ios_api }}barcodes-result-item.html) in the DSCapturedResult. |
| [`recognizedTextLinesResult`](#recognizedtextlinesresult) | *DSRecognizedTextLinesResult* | A [`DSRecognizedTextLinesResult`]({{ site.dlr_ios_api }}recognized-text-lines-result.html) object that contains all the [`DSTextLinesResultItems`]({{ site.dlr_ios_api }}text-lines-result-item.html) in the DSCapturedResult. |
| [`detectedQuadsResult`](#detectedquadsresult) | *DSDetectedQuadsResult* | A [`DSDetectedQuadsResult`]({{ site.ddn_ios_api }}detected-quads-result.html) object that contains all the [`DSDetectedQuadResultItem`]({{ site.ddn_ios_api }}detected-quad-result-item.html) in the DSCapturedResult. |
| [`normalizedImagesResult`](#normalizedimagesresult) | *DSNormalizedImagesResult* | A [`DSNormalizedImagesResult`]({{ site.ddn_ios_api }}normalized-images-result.html) object that contains all the [`DSNormalizedImageResultItem`]({{ site.ddn_ios_api }}normalized-image-result-item.html) in the DSCapturedResult. |
| [`parsedResult`](#parsedresult) | *DSParsedResult* | A [`DSParsedResult`]({{ site.dcp_ios_api }}parsed-result.html) object that contains all the [`DSParsedResultItem`]({{ site.dcp_ios_api }}parsed-result-item.html) in the DSCapturedResult. |

### originalImageHashId

The hash ID of the original image which can be used to get the original image via the [IntermediateResultManager]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/intermediate-result-manager.html) class.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy, readonly) NSString *originalImageHashId;
```
2. 
```swift
var originalImageHashId: String { get }
```

### originalImageTag

The [DSImageTag]({{ site.dcv_ios_api }}core/basic-structures/image-tag.html) of the original image that records information such as the image ID of the original image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, readonly) DSImageTag *originalImageTag;
```
2. 
```swift
var originalImageTag: ImageTag { get }
```

### items

An array of [DSCapturedResultItem]({{ site.dcv_ios_api }}core/basic-structures/captured-result-item.html), which is the basic unit of the captured results. A DSCapturedResultItem can be an original image, a decoded barcode, a recognized text, a detected quad, a normalized image, or a parsed result. View DSCapturedResultItemType for all available types.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, nullable, readonly) NSArray<DSCapturedResultItem *> *items;
```
2. 
```swift
var items: [CapturedResultItem]? { get }
```

### rotationTransformMatrix

The rotation transformation matrix of the original image relative to the rotated image. View [CGAffineTransform](https://developer.apple.com/documentation/corefoundation/cgaffinetransform) for more info.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign, readonly) CGAffineTransform rotationTransformMatrix;
```
2. 
```swift
var rotationTransformMatrix: CGAffineTransform { get }
```

### errorCode

Get the error code of this result. A `CapturedResult` will carry error information when the license module is missing or the process timeout.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) NSInteger errorCode;
```
2. 
```swift
var errorCode: Int { get }
```

### errorMessage

Get the error message of this result. A `CapturedResult` will carry error information when the license module is missing or the process timeout.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) NSString * errorMessage;
```
2. 
```swift
var errorMessage: String { get }
```

### decodedBarcodesResult

A [`DSDecodedBarcodesResult`]({{site.dbr_ios_api}}decoded-barcodes-result.html) object that contains all the [`DSBarcodesResultItems`]({{ site.dbr_ios_api }}barcode-result-item.html) in the DSCapturedResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, strong, nullable) DSDecodedBarcodesResult * decodedBarcodesResult;
```
2. 
```swift
var decodedBarcodesResult: DecodedBarcodesResult? { get }
```

### recognizedTextLinesResult

A [`DSRecognizedTextLinesResult`]({{site.dlr_ios_api}}recognized-text-lines-result.html) object that contains all the [`DSTextLinesResultItems`]({{ site.dlr_ios_api }}text-line-result-item.html) in the DSCapturedResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, strong, nullable) DSRecognizedTextLinesResult * recognizedTextLinesResult;
```
2. 
```swift
var recognizedTextLinesResult: RecognizedTextLinesResult? { get }
```

### detectedQuadsResult

A [`DSDetectedQuadsResult`]({{site.ddn_ios_api}}detected-quads-result.html) object that contains all the [`DSDetectedQuadResultItem`]({{ site.ddn_ios_api }}detected-quad-result-item.html) in the DSCapturedResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, strong, nullable) DSDetectedQuadsResult * detectedQuadsResult;
```
2. 
```swift
var detectedQuadsResult: DetectedQuadsResult? { get }
```

### normalizedImagesResult

A [`DSNormalizedImagesResult`]({{site.ddn_ios_api}}normalized-images-result.html) object that contains all the [`DSNormalizedImageResultItem`]({{ site.ddn_ios_api }}normalized-image-result-item.html) in the DSCapturedResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, strong, nullable) DSNormalizedImagesResult * normalizedImagesResult;
```
2. 
```swift
var normalizedImagesResult: NormalizedImagesResult? { get }
```

### parsedResult

A [`DSParsedResult`]({{site.dcp_ios_api}}parsed-result.html) object that contains all the [`DSParsedResultItem`]({{ site.dcp_ios_api }}parsed-result-item.html) in the DSCapturedResult.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, strong, nullable) DSParsedResult * parsedResult;
```
2. 
```swift
var parsedResult: ParsedResult? { get }
```
