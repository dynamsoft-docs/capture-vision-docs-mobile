---
layout: default-layout
title: DSPredetectedRegionsUnit - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSPredetectedRegionsUnit of Dynamsoft Capture Vision iOS represents a unit that contains a collection of pre-detected regions.
keywords: pre-detected regions, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSPredetectedRegionsUnit

The `DSPredetectedRegionsUnit` class extends the `DSIntermediateResultUnit` class and represents a unit of intermediate result specifically for pre-detected regions.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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
| [`getPredetectedRegions`](#getpredetectedregions) | Gets an array of [`DSPredetectedRegionElement`]({{ site.dcv_ios_api }}core/intermediate-results/predetected-region-element.html) objects, each representing a pre-detected region detected within the image. |
| [`getCount`](#getcount) | Returns the number of pre-detected regions. |
| [`getPredetectedRegion`](#getpredetectedregion) | Returns a pre-detected region. |
| [`removeAllPredectedRegions`](#removeallpredectedregions) | Removes all pre-detected regions. |
| [`removePredetectedRegion`](#removepredetectedregion) | Removes the pre-detected region at the specified index. |
| [`addPredetectedRegion`](#addpredetectedregion) | Adds a pre-detected region. |
| [`setPredetectedRegion`](#setpredetectedregion) | Sets a pre-detected region. |

## Inherited Methods

The following methods are inherited from class [`DSIntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`getHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image associated with this unit. |
| [`getOriginalImageTag`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the tag associated with the original image. |
| [`getType`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`IntermediateResultUnitType`]({{ site.dcv_ios_api }}core/enum/intermediate-result-unit-type.html?lang=objc,swift). |
| [`getTransformMatrix`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`DSTransformMatrixType`]({{ site.dcv_ios_api }}core/enum/transform-matrix-type.html). |
| [`clone`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`replace`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the content of the intermediate result unit. |

### getPredetectedRegions

Get an array of [`DSPredetectedRegionElement`]({{ site.dcv_ios_api }}core/intermediate-results/predetected-region-element.html) objects, each representing a pre-detected region detected within the image.

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
