---
layout: default-layout
title: DSTextureRemovedGrayscaleImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSTextureRemovedGrayscaleImageUnit of Dynamsoft Core Module represents a unit that contains a texture-removed grayscale image. It is derived from the DSIntermediateResultUnit class.
keywords: texture-removed grayscale image, unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextureRemovedGrayscaleImageUnit

The `DSTextureRemovedGrayscaleImageUnit` class extends the `DSIntermediateResultUnit` class and represents a texture-removed grayscale image unit.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSTextureRemovedGrayscaleImageUnit: DSIntermediateResultUnit
```
2. 
```swift
class TextureRemovedGrayscaleImageUnit : IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`setImageData`](#setimagedata) | Sets the image data for the texture-removed grayscale image. |
| [`getImageData`](#getimagedata) | Gets the image data for the texture-removed grayscale image. |

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

Sets the image data for the texture-removed grayscale image.

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
func setImageData(_ imageData: ImageData?) -> Int
```

**Parameters**

`imageData`: A `DSImageData` object as the image data of the texture removed grayscale image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getImageData

Gets the image data for the texture-removed grayscale image.

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
func getImageData() -> ImageData?
```

**Return Value**

A `DSImageData` object that describes the texture removed grayscale image.
