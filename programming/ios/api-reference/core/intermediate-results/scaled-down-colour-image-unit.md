---
layout: default-layout
title: DSScaledColourImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSScaledColourImageUnit of Dynamsoft Core Module represents a unit that contains a down-scaled colour image.
keywords: scaled down colour image unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSScaledColourImageUnit

The `ScaledDownColourImageUnit` class extends the `IntermediateResultUnit` class and represents a scaled-down colour image unit.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSScaledColourImageUnit : DSIntermediateResultUnit
```
2. 
```swift
class ScaledDownColourImageUnit : DSIntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`setImageData`](#setimagedata) | Sets the image data for the scaled-down colour image. |
| [`getImageData`](#getimagedata) | Gets the image data for the scaled-down colour image. |

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

### setImageData

Sets the image data for the scaled-down colour image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setImageData:(DSImageData *)imageData;
```
2. 
```swift
func setImageData(_ imageData: DSImageData?) -> Int
```

**Parameters**

`imageData`: A `DSImageData` object as the image data of the down-scaled colour image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getImageData

Gets the image data for the scaled-down colour image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSImageData *)getImageData;
```
2. 
```swift
func getImageData() -> DSImageData?
```

**Return Value**

The `DSImageData` for the scaled-down colour image.
