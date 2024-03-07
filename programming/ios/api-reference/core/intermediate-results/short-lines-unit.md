---
layout: default-layout
title: DSShortLinesUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSShortLinesUnit of Dynamsoft Core Module represents a unit that contains the detected short lines.
keywords: short lines, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSShortLinesUnit

The class `DSShortLinesUnit` represents a unit that contains the detected short lines.

## Definition

*Assembly:* DynamsoftCore.framework

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
| [`getShortLines`](#getshortlines) | Returns the short lines in this unit. |
| [`getCount`](#getcount) | Returns the number of short lines in this unit. |
| [`getShortLine`](#getshortline) | Returns the short line at the specified index. |
| [`removeAllShortLines`](#removeallshortlines) | Removes all the short lines in this unit. |
| [`removeShortLine`](#removeshortline) | Removes the short line at the specified index. |
| [`addShortLine`](#addshortline) | Adds a short line to this unit. |
| [`setShortLine`](#setshortline) | Sets the short line at the specified index. |

### getShortLines

Returns the short lines in this unit.

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

An array of `DSLineSegment` objects as the short lines in this unit.

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
