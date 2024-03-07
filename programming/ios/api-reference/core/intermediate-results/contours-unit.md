---
layout: default-layout
title: DSContoursUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSContoursUnit of Dynamsoft Core Module represents a unit that contains contours as intermediate results.
keywords: contours unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSContoursUnit

The `DSContoursUnit` class represents a unit that contains contours as intermediate results. It is derived from the `DSIntermediateResultUnit` class.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSContoursUnit: DSIntermediateResultUnit
```
2. 
```swift
class ContoursUnit: IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`getContours`](#getcontours) | Gets the array of `DSContour` objects. |
| [`getHierarchies`](#gethierarchies) | Gets the array of `DSVector4` objects. |
| [`setContours`](#setcontours) | Sets the contours. |

### getContours

Get an array of `DSContour` objects.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSContour*>*)getContours;
```
2. 
```swift
func getContours() -> [Contour]?
```

**Return Value**

An array of `DSContour` objects.

### setContours

Sets the contours.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setContours:(NSArray<DSContour*>*)contours
            hierarchies:(NSArray<Vector4*>*)hierarchies
  matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setContours(_ contours: [Contour]?, hierarchies: [Vector4]?, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`contours`: An array of `DSContour` objects.

`hierarchies`: The contour hierarchies as an array of `DSVector4` objects.

`matrixToOriginalImage`: The matrix to original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getHierarchies

Gets the array of `DSVector4` objects.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSVector4*>*)getHierarchies;
```
2. 
```swift
func getHierarchies() -> [Vector4]?
```

**Return Value**

The contour hierarchies as an array of `DSVector4` objects.
