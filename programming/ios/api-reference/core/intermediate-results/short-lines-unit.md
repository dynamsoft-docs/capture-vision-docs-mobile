---
layout: default-layout
title: DSShortLinesUnit - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSShortLinesUnit of Dynamsoft Capture Vision iOS represents a unit that contains the detected short lines.
keywords: short lines, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSShortLinesUnit

The `DSShortLinesUnit` class extends the `DSIntermediateResultUnit` class and represents a unit of intermediate result specifically for short lines.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSShortLinesUnit: DSIntermediateResultUnit
```
2. 
```swift
class ShortLinesUnit: IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`getShortLines`](#getshortlines) | Gets an array of [`DSLineSegment`]({{ site.dcv_ios_api }}core/basic-structure/line-segment.html) objects, each representing a short line detected within the image. |
| [`getCount`](#getcount) | Returns the number of short lines in this unit. |
| [`getShortLine`](#getshortline) | Returns the short line at the specified index. |
| [`removeAllShortLines`](#removeallshortlines) | Removes all the short lines in this unit. |
| [`removeShortLine`](#removeshortline) | Removes the short line at the specified index. |
| [`addShortLine`](#addshortline) | Adds a short line to this unit. |
| [`setShortLine`](#setshortline) | Sets the short line at the specified index. |

## Inherited Methods

The following methods are inherited from class [`IntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`getHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image associated with this unit. |
| [`getOriginalImageTag`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the tag associated with the original image. |
| [`getType`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`IntermediateResultUnitType`]({{ site.dcv_ios_api }}core/enum/intermediate-result-unit-type.html?lang=objc,swift). |
| [`getTransformMatrix`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`DSTransformMatrixType`]({{ site.dcv_ios_api }}core/enum/transform-matrix-type.html). |
| [`clone`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`replace`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the content of the intermediate result unit. |

### getShortLines

Gets an array of [`DSLineSegment`]({{ site.dcv_ios_api }}core/basic-structure/line-segment.html) objects, each representing a short line detected within the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSLineSegment*>*)getShortLines;
```
2. 
```swift
func getShortLines() -> [LineSegment]?
```

**Return Value**

An array of [`DSLineSegment`]({{ site.dcv_ios_api }}core/basic-structure/line-segment.html) objects.

### getCount

Returns the number of short lines in this unit.

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

`NSInteger` as the number of short lines in this unit.

### getShortLine

Returns the short line at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSLineSegment *)getShortLine:(NSInteger)index;
```
2. 
```swift
func getShortLine(_ index: Int) -> LineSegment?
```

**Parameters**

`index`: The index of the short line.

**Return Value**

A `DSLineSegment` object as the short line at the specified index.

### removeAllShortLines

Removes all the short lines in this unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)removeAllShortLines;
```
2. 
```swift
func removeAllShortLines()
```

### removeShortLine

Removes the short line at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)removeShortLine:(NSInteger)index;
```
2. 
```swift
func removeShortLine(_ index: Int)
```

**Parameters**

`index`: The index of the short line.

### addShortLine

Adds a short line to this unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)addShortLine:(DSLineSegment*)line
   matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func addShortLine(_ line: LineSegment, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`line`: A `DSLineSegment` object as the short line to be added.

`matrixToOriginalImage`: A `CGAffineTransform` object as the transformation matrix from the original image to the image in this unit.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setShortLine

Sets the short line at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setShortLine:(NSInteger)index
                    line:(DSLineSegment*)line
   matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setShortLine(_ index: Int, line: LineSegment, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`index`: The index of the short line.

`line`: A `DSLineSegment` object as the short line to be set.

`matrixToOriginalImage`: A `CGAffineTransform` object as the transformation matrix from the original image to the image in this unit.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
