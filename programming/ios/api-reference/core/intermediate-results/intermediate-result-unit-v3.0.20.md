---
layout: default-layout
title: DSIntermediateResultUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSIntermediateResultUnit of Dynamsoft Core Module represents an intermediate result unit used in image processing, which is an abstract base class with multiple subclasses.
keywords: intermediate result unit, image processing, objective-c, swift
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
| [`originalImageHashId`](#originalimagehashid) | *NSString \** | The hash ID of the original image. You can use this ID to get the original image via IntermediateResultManager class. |
| [`originalImageTag`](#originalimagetag) | *DSImageTag \** | The image tag of the original image. |
| [`type`](#type) | *DSIntermediateResultUnitType* | The type of the intermediate result unit. |

## Methods

| Method | Description |
|------- |-------------|
| [`getTransformMatrix`](#gettransformmatrix) | Gets the transformation matrix via [`DSTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html). |
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

### originalImageHashId

The hash ID of the original image. You can use this ID to get the original image via IntermediateResultManager class.

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
var originalImageHashId: String? { get }
```

### originalImageTag

The image tag of the original image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, readonly, nullable) DSImageTag *originalImageTag;
```
2. 
```swift
var originalImageTag: ImageTag? { get }
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

### getTransformMatrix

Gets the transformation matrix via [`DSTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(CGAffineTransform)getTransformMatrix:(DSTransformMatrixType)matrixType;
```
2. 
```swift
func getTransformMatrix(DSTransformMatrixType matrixType) -> CGAffineTransform
```

**Parameters**

`[in] matrixType`: The transform matrix type.

**Return Value**

The corresponding transformation matrices are as follows:

- local image to original image
- original image to local image
- rotated image to original image
- original image to rotated image

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
