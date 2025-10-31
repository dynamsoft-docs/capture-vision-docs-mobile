---
layout: default-layout
title: DSCapturedResultBase - Dynamsoft Core Module iOS Edition API Reference
description: The class DSCapturedResultBase of Dynamsoft Core Module is the base class of all types of captured results.
keywords: captured result base, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# DSCapturedResultBase

The `DSCapturedResultBase` class is the base class of all types of captured results.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCapturedResultBase : NSObject
```
2. 
```swift
class CapturedResultBase : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`originalImageHashId`](#originalimagehashid) | *NSString \** | The hash id of the original image. |
| [`originalImageTag`](#originalimagetag) | *DSImageTag \** | The [DSImageTag](image-tag.md) of the original image. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`](#errorcode) | *NSInteger* | Get the error code of this result. |
| [`errorMessage`](#errormessage) | *NSString \** | Get the error message of this result. |

### originalImageHashId

The hash id of the original image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, copy, readonly) NSString *originalImageHashId;
```
2. 
```swift
var originalImageHashId: String { get }
```

### originalImageTag

The [DSImageTag](image-tag.md) of the original image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, strong, nullable) DSImageTag *originalImageTag;
```
2. 
```swift
var originalImageTag: ImageTag { get }
```

### rotationTransformMatrix

The rotation transformation matrix of the original image relative to the rotated image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) CGAffineTransform rotationTransformMatrix;
```
2. 
```swift
var rotationTransformMatrix: CGAffineTransform { get }
```

### errorCode

The error code of this result.

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

The error message of this result.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, copy, nullable) NSString * errorMessage;
```
2. 
```swift
var errorMessage: String { get }
```
