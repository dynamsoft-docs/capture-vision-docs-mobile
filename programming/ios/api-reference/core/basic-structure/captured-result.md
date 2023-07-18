---
layout: default-layout
Title: DSCapturedResult - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSCapturedResult of Dynamsoft Core Module represents the result of a capture operation on an image, which contains multiple items such as barcode, text line, detected quad, normalized image, raw image, parsed item, etc.
Keywords: captured result, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCapturedResult

The `DSCapturedResult` class represents the result of a capture operation on an image. Internally, `DSCapturedResult` stores an array that contains multiple items, each of which may be a barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

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
| [`sourceImageHashId`](#sourceimagehashid) | *NSString \** | The hash id of the source image. You can use this ID to get the source image via `IntermediateResultManager` class. |
| [`sourceImageTag`](#sourceimagetag) | *DSImageTag* | The tag of the source image that records the information of the source image. |
| [`items`](#items) | *NSArray<DSCapturedResultItem*> \** | An array of `DSCapturedResultItems`, which are the basic unit of the captured results. A `DSCapturedResultItem` can be a raw image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View DSCapturedResultItemType for all available types. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image. |

### sourceImageHashId

The hash id of the source image. You can use this ID to get the source image via IntermediateResultManager class.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy, readonly) NSString *sourceImageHashId;
```
2. 
```swift
var sourceImageHashId: String { get }
```

### sourceImageTag

The tag of the source image that records the information of the source image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, readonly) DSImageTag *sourceImageTag;
```
2. 
```swift
var sourceImageTag: ImageTag { get }
```

### items

An array of DSCapturedResultItems, which are the basic unit of the captured results. A DSCapturedResultItem can be a raw image, a decoded barcode, a recognized text, a detected quad, a normalized image or a parsed result. View DSCapturedResultItemType for all available types.

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

The rotation transformation matrix of the original image relative to the rotated image.

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
