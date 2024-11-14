---
layout: default-layout
title: DSLineSegmentsUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSLineSegmentsUnit of Dynamsoft Core Module represents a collection of line segments in 2D space.
keywords: line segments, 2D space, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLineSegmentsUnit

The `DSLineSegmentsUnit` class extends the `DSIntermediateResultUnit` class and represents a unit of intermediate result specifically for line segments.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSLineSegmentsUnit: DSIntermediateResultUnit
```
2. 
```swift
class LineSegmentsUnit : IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`getLineSegments`](#getlinesegments) | Gets an array of [`DSLineSegment`]({{ site.dcv_ios_api }}core/basic-structures/line-segment.html) objects, each representing a segment of a line detected within the image. |
| [`getCount`](#getcount) | Returns the number of line segments. |
| [`getLineSegment`](#getlinesegment) | Returns the line segment at the specified index. |
| [`removeAllLineSegments`](#removealllinesegments) | Removes all line segments. |
| [`removeLineSegment`](#removelinesegment) | Removes the line segment at the specified index. |
| [`addLineSegment`](#addlinesegment) | Adds a line segment. |
| [`setLineSegment`](#setlinesegment) | Sets a line segment. |

## Inherited Methods

The following methods are inherited from class [`DSIntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`getHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image associated with this unit. |
| [`getOriginalImageTag`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the tag associated with the original image. |
| [`getType`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`IntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=objc,swift). |
| [`getTransformMatrix`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`DSTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html). |
| [`clone`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`replace`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the content of the intermediate result unit. |

### getLineSegments

Get an array of [`DSLineSegment`]({{ site.dcv_ios_api }}core/basic-structure/line-segment.html) objects, each representing a segment of a line detected within the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSLineSegment*>*)getLineSegments;
```
2. 
```swift
func getLineSegments() -> [LineSegment]?
```

**Return Value**

An array of `DSLineSegment` objects.

### getCount

Returns the number of line segments.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)getCount;
```
2. 
```swift
func getCount() -> Int
```

**Return Value**

Returns the number of line segments.

### getLineSegment

Returns the line segment at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSLineSegment *)getLineSegment:(NSInteger)index;
```
2. 
```swift
func getLineSegment(_ index: Int) -> LineSegment?
```

**Parameters**

`index`: The index of the line segment.

**Return Value**

Returns the line segment at the specified index.

### removeAllLineSegments

Removes all line segments.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)removeAllLineSegments;
```
2. 
```swift
func removeAllLineSegments()
```

### removeLineSegment

Removes the line segment at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)removeLineSegment:(NSInteger)index;
```
2. 
```swift
func removeLineSegment(_ index: Int) -> Int
```

**Parameters**

`index`: The index of the line segment.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addLineSegment

Adds a line segment.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)addLineSegment:(DSLineSegment *)line
    matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func addLineSegment(_ line: LineSegment, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`line`: A `DSLineSegment` object as the line segment.

`matrixToOriginalImage`: A `CGAffineTransform` object as the matrix to original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setLineSegment

Sets a line segment.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setLineSegment:(NSInteger)index
                      line:(DSLineSegment *)line
    matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setLineSegment(_ index: Int, line: LineSegment, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`index`: The index of the line segment.

`line`: A `DSLineSegment` object as the line segment.

`matrixToOriginalImage`: A `CGAffineTransform` object as the matrix to original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
