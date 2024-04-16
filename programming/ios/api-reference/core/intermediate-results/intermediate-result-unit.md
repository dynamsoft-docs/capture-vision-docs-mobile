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

## Methods

| Method | Description |
|------- |-------------|
| [`getHashId`](#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image associated with this unit. |
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the image tag of the original image. |
| [`getType`](#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`IntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=objc,swift). |
| [`getTransformMatrix`](#gettransformmatrix) | Gets the transformation matrix via [`DSTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html). |
| [`clone`](#clone) | Creates a copy of the intermediate result unit. |
| [`replace`](#replace) | Replaces the content of the intermediate result unit. |

### getHashId

Gets the hash ID of the unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSString*)getHashId;
```
2. 
```swift
func getHashId() -> String
```

### getOriginalImageHashId

Get the hash ID of the original image. You can use this ID to get the original image via `IntermediateResultManager` class.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSString*)getOriginalImageHashId;
```
2. 
```swift
func getOriginalImageHashId() -> String
```

### getOriginalImageTag

Gets the image tag of the original image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSImageTag*)getOriginalImageTag;
```
2. 
```swift
func getOriginalImageTag() -> ImageTag?
```

**Return Value**

The image tag of the original image.

### getType

Gets the type of the intermediate result unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(DSIntermediateResultUnitType)getType;
```
2. 
```swift
func getType() -> DSIntermediateResultUnitType
```

**Return Value**

The type of the intermediate result unit.

### getTransformMatrix

Gets the transformation matrix via [`DSTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(CGAffineTransform)getTransformMatrix:(DSTransformMatrixType)type;
```
2. 
```swift
func getTransformMatrix(_ type: DSTransformMatrixType) -> CGAffineTransform
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

### replace

Replaces the content of the intermediate result unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)replace:(DSIntermediateResultUnit*)oldUnit;
```
2. 
```swift
func replace(_ oldUnit: DSIntermediateResultUnit) -> NSInteger
```

**Parameters**

`[in] oldUnit`: The old unit.

**Return Value**

A NSInteger that indicates whether the replace is success. If success returns 0, otherwise returns the error code.
