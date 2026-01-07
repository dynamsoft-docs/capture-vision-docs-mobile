---
layout: default-layout
title: DSTextureDetectionResultUnit - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSTextureDetectionResultUnit of Dynamsoft Capture Vision iOS represents an intermediate result unit for texture detection, which contains the x-direction spacing and y-direction spacing of the texture stripes.
keywords: texture detection, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextureDetectionResultUnit

The `DSTextureDetectionResultUnit` class extends the `DSIntermediateResultUnit` class and represents a texture-detection result unit. This class captures the results of texture analysis, specifically the spacing of texture patterns in both the x and y directions.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(TextureDetectionResultUnit)
@interface DSTextureDetectionResultUnit: DSIntermediateResultUnit
```
2. 
```swift
class TextureDetectionResultUnit : IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`getXSpacing`](#xspacing) | Gets the detected horizontal distance in pixels between consecutive texture patterns, providing an indication of the texture's density and orientation within the image. |
| [`setXSpacing`](#xspacing) | Sets the x-direction spacing of the texture. |
| [`getYSpacing`](#yspacing) | Gets the spacing between texture stripes in the y-direction. Similar to `xSpacing`, this value measures the vertical distance between texture patterns. texture's characteristics and spatial distribution. |
| [`setYSpacing`](#yspacing) | Sets the y-direction spacing of the texture. |

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

### getXSpacing

Gets the detected horizontal distance in pixels between consecutive texture patterns, providing an indication of the texture's density and orientation within the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)getXSpacing;
```
2. 
```swift
func getXSpacing() -> Int
```

### setXSpacing

Sets the x-direction spacing of the texture.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)setXSpacing:(NSInteger)xSpacing;
```
2. 
```swift
func setXSpacing(xSpacing: Int)
```

### getYSpacing

Sets the spacing between texture stripes in the y-direction. Similar to `xSpacing`, this value measures the vertical distance between texture patterns. texture's characteristics and spatial distribution.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)getYSpacing;
```
2. 
```swift
func getYSpacing() -> Int
```

### setYSpacing

Sets the y-direction spacing of the texture.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)setYSpacing:(NSInteger)ySpacing;
```
2. 
```swift
func setYSpacing(ySpacing: Int)
```
