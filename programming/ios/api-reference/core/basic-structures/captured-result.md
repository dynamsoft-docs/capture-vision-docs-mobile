---
layout: default-layout
title: DSCapturedResult - Dynamsoft Core Module iOS Edition API Reference
description: The class DSCapturedResult of Dynamsoft Core Module represents the result of a capture operation on an image, which contains multiple items such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.
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
| [`originalImageTag`](#originalimagetag) | *DSImageTag* | The [DSImageTag](image-tag.md) of the original image that records information such as the image ID of the original image. |
| [`items`](#items) | *NSArray<DSCapturedResultItem*> \** | An array of `DSCapturedResultItems`, which are the basic unit of the captured results. A `DSCapturedResultItem` can be a original image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View DSCapturedResultItemType for all available types. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`](#errorcode) | *NSInteger* | Get the error code of this result. |
| [`errorMessage`](#errormessage) | *NSString \** | Get the error message of this result. |

### originalImageHashId

The hash ID of the original image which can be used to get the original image via the [IntermediateResultManager](../intermediate-results/intermediate-result-manager.md) class.

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

The [DSImageTag](image-tag.md) of the original image that records information such as the image ID of the original image.

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

An array of [DSCapturedResultItem](captured-result-item.md), which is the basic unit of the captured results. A DSCapturedResultItem can be an original image, a decoded barcode, a recognized text, a detected quad, a normalized image, or a parsed result. View DSCapturedResultItemType for all available types.

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
