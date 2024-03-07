---
layout: default-layout
title: DSEnhancedGrayscaleImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSEnhancedGrayscaleImageUnit of Dynamsoft Core Module represents a unit that contains a grayscale enhanced image.
keywords: enhanced grayscale image unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSEnhancedGrayscaleImageUnit

The `DSEnhancedGrayscaleImageUnit` class represents a unit that contains a grayscale enhanced image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSEnhancedGrayscaleImageUnit : DSIntermediateResultUnit
```
2. 
```swift
class EnhancedGrayscaleImageUnit : IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`setImageData`](#setimagedata) | Sets the image data of the enhanced grayscale image. |
| [`getImageData`](#getimagedata) | Returns the image data of the enhanced grayscale image. |

### setImageData

Set the image data of the enhanced grayscale image.

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

`imageData`: A `DSImageData` object as the image data of the enhanced grayscale image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getImageData

Get the image data of the enhanced grayscale image.

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

The image data of the enhanced grayscale image.
