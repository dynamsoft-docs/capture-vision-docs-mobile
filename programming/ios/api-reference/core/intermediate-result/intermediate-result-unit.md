---
layout: default-layout
Title: DSIntermediateResultUnit - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSIntermediateResultUnit of Dynamsoft Core Module represents an intermediate result unit used in image processing, which is an abstract base class with multiple subclasses.
Keywords: intermediate result unit, image processing, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIntermediateResultUnit

The `DSIntermediateResultUnit` class represents an intermediate result unit used in image processing. It is an abstract base class with multiple subclasses, each representing a different type of unit such as pre-detected regions, localized barcodes, decoded barcodes, localized text lines, binary image, gray image, etc.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSIntermediateResultUnit : NSObject
```
2. 
```swift
class IntermediateResultUnit : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`hashId`](#hashid) | *NSString \** | The hash ID of the unit. |
| [`sourceImageHashId`](#sourceimagehashid) | *NSString \** | The hash ID of the source image. You can use this ID to get the source image via IntermediateResultManager class. |
| [`sourceImageTag`](#sourceimagetag) | *DSImageTag \** | The image tag of the source image. |
| [`type`](#type) | *DSIntermediateResultUnitType* | The type of the intermediate result unit. |
| [`localToSourceImageTransformMatrix`](#localtosourceimagetransformmatrix) | *CGAffineTransform* | The transformation matrix from local to source image coordinates. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image. |

## Methods

| Method | Description |
|------- |-------------|
| [`clone`](#clone) | Creates a copy of the intermediate result unit. |

### hashId

The hash ID of the unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, copy, readonly) NSString *hashId;
```
2. 
```swift
var hashId: String? { get }
```

### sourceImageHashId

The hash ID of the source image. You can use this ID to get the source image via IntermediateResultManager class.

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
var sourceImageHashId: String? { get }
```

### sourceImageTag

The image tag of the source image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, readonly, nullable) DSImageTag *sourceImageTag;
```
2. 
```swift
var sourceImageTag: ImageTag? { get }
```

### type

The type of the intermediate result unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign, readonly) EnumIntermediateResultUnitType type;
```
2. 
```swift
var type: EnumIntermediateResultUnitType { get }
```

### localToSourceImageTransformMatrix

The transformation matrix from local to source image coordinates.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign, readonly) CGAffineTransform localToSourceImageTransformMatrix;
```
2. 
```swift
var localToSourceImageTransformMatrix: CGAffineTransform { get }
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

### clone

Creates a copy of the intermediate result unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSIntermediateResultUnit*)clone;
```
2. 
```swift
func clone() -> IntermediateResultUnit
```

**Return Value**

A copy of the intermediate result unit.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
DSIntermediateResultUnit *unitCopy = [unit clone];
```
2. 
```swift
let unitCopy = unit.clone()
```
