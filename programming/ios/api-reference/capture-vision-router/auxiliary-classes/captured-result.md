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

*Assembly:* DynamsoftCore.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCapturedResult : DSCapturedResultBase
```
2. 
```swift
class CapturedResult : CapturedResultBase
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`items`](#items) | *NSArray<DSCapturedResultItem*> \** | An array of `DSCapturedResultItems`, which are the basic item of the captured results. A `DSCapturedResultItem` can be an original image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View DSCapturedResultItemType for all available types. |
| [`decodedBarcodesResult`](#decodedbarcodesresult) | *DSDecodedBarcodesResult* | A [`DSDecodedBarcodesResult`]({{ site.dbr_ios_api }}decoded-barcodes-result.html) object that contains all the [`DSBarcodeResultItems`]({{ site.dbr_ios_api }}barcode-result-item.html) in the DSCapturedResult. |
| [`recognizedTextLinesResult`](#recognizedtextlinesresult) | *DSRecognizedTextLinesResult* | A [`DSRecognizedTextLinesResult`]({{ site.dlr_ios_api }}recognized-text-lines-result.html) object that contains all the [`DSTextLineResultItems`]({{ site.dlr_ios_api }}text-line-result-item.html) in the DSCapturedResult. |
| [`detectedQuadsResult`](#detectedquadsresult) | *DSDetectedQuadsResult* | A [`DSDetectedQuadsResult`]({{ site.ddn_ios_api }}detected-quads-result.html) object that contains all the [`DSDetectedQuadResultItem`]({{ site.ddn_ios_api }}detected-quad-result-item.html) in the DSCapturedResult. |
| [`normalizedImagesResult`](#normalizedimagesresult) | *DSNormalizedImagesResult* | A [`DSNormalizedImagesResult`]({{ site.ddn_ios_api }}normalized-images-result.html) object that contains all the [`DSNormalizedImageResultItem`]({{ site.ddn_ios_api }}normalized-image-result-item.html) in the DSCapturedResult. |
| [`parsedResult`](#parsedresult) | *DSParsedResult* | A [`DSParsedResult`]({{ site.dcp_ios_api }}parsed-result.html) object that contains all the [`DSParsedResultItem`]({{ site.dcp_ios_api }}parsed-result-item.html) in the DSCapturedResult. |

The following attributes are inherited from [`DSCapturedResultBase`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html):

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`originalImageHashId`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#originalimagehashid) | *NSString \** | The hash id of the original image. |
| [`originalImageTag`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#originalimagetag) | *DSImageTag \** | The [DSImageTag](image-tag.md) of the original image. |
| [`rotationTransformMatrix`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#errorcode) | *NSInteger* | Get the error code of this result. |
| [`errorMessage`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#errormessage) | *NSString \** | Get the error message of this result. |

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
