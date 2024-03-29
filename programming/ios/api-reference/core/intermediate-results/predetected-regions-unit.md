---
layout: default-layout
title: DSPredetectedRegionsUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSPredetectedRegionsUnit of Dynamsoft Core Module represents a unit that contains a collection of pre-detected regions.
keywords: pre-detected regions, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSPredetectedRegionsUnit

The `DSPredetectedRegionsUnit` class represents a unit that contains a collection of pre-detected regions.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSPredetectedRegionsUnit: DSIntermediateResultUnit
```
2. 
```swift
class PredetectedRegionsUnit: IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`getPredetectedRegions`](#getpredetectedregions) | Gets an array of `DSPredetectedRegionElement` objects that indicates the pre-detected regions. |
| [`getCount`](#getcount) | Returns the number of pre-detected regions. |
| [`getPredetectedRegion`](#getpredetectedregion) | Returns a pre-detected region. |
| [`removeAllPredectedRegions`](#removeallpredectedregions) | Removes all pre-detected regions. |
| [`removePredetectedRegion`](#removepredetectedregion) | Removes the pre-detected region at the specified index. |
| [`addPredetectedRegion`](#addpredetectedregion) | Adds a pre-detected region. |
| [`setPredetectedRegion`](#setpredetectedregion) | Sets a pre-detected region. |

### getPredetectedRegions

Get an array of `DSPredetectedRegionElement` objects that indicates the pre-detected regions.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSPredetectedRegionElement*>*)getPredetectedRegions;
```
2. 
```swift
func getPredetectedRegions() -> [PredetectedRegionElement]?
```

**Return Value**

An array of `DSPredetectedRegionElement` objects that indicates the pre-detected regions.

### getCount

Returns the number of pre-detected regions.

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

Returns the number of pre-detected regions.

### getPredetectedRegion

Returns a pre-detected region.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSPredetectedRegionElement*)getPredetectedRegion:(NSInteger)index;
```
2. 
```swift
func getPredetectedRegion(_ index: Int) -> PredetectedRegionElement?
```

**Parameters**

`index`: Specify the index of the pre-detected region.

**Return Value**

Returns the pre-detected region at the specified index.

### removeAllPredectedRegions

Removes all pre-detected regions.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)removeAllPredectedRegions;
```
2. 
```swift
func removeAllPredectedRegions()
```

### removePredetectedRegion

Removes the pre-detected region at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)removePredetectedRegion:(NSInteger)index;
```
2. 
```swift
func removePredetectedRegion(_ index: Int) -> Int
```

**Parameters**

`index`: Specify the index of the pre-detected region.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addPredetectedRegion

Adds a pre-detected region.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)addPredetectedRegion:(DSPredetectedRegionElement*)element
           matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func addPredetectedRegion(_ element: PredetectedRegionElement, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`element`: A `DSPredetectedRegionElement` object that indicates the pre-detected region.

`matrixToOriginalImage`: A `CGAffineTransform` object that indicates the transformation matrix from the original image to the pre-detected region.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setPredetectedRegion

Sets a pre-detected region.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setPredetectedRegion:(NSInteger)index
                         element:(DSPredetectedRegionElement*)element
           matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setPredetectedRegion(_ index: Int, element: PredetectedRegionElement, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`index`: Specify the index of the pre-detected region.

`element`: A `DSPredetectedRegionElement` object that indicates the pre-detected region.

`matrixToOriginalImage`: A `CGAffineTransform` object that indicates the transformation matrix from the original image to the pre-detected region.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
