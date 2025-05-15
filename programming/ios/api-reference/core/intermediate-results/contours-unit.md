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

The `DSContoursUnit` class extends the `DSIntermediateResultUnit` class and represents a unit of contours, which are collections of points that define the shape of an object in an image.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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

## Inherited Methods

The following methods are inherited from class [`IntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`getHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image associated with this unit. |
| [`getOriginalImageTag`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the tag associated with the original image. |
| [`getType`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`IntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=objc,swift). |
| [`getTransformMatrix`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`DSTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html). |
| [`clone`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`replace`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the content of the intermediate result unit. |

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
