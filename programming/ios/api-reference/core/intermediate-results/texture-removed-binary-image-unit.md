---
layout: default-layout
title: DSTextureRemovedBinaryImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSTextureRemovedBinaryImageUnit of Dynamsoft Core Module represents a unit that contains a texture-removed binary image.
keywords: texture-removed binary image, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextureRemovedBinaryImageUnit

The `DSTextureRemovedBinaryImageUnit` class represents a unit that contains a texture-removed binary image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(TextureRemovedBinaryImageUnit)
@interface DSTextureRemovedBinaryImageUnit: DSIntermediateResultUnit
```
2. 
```swift
class TextureRemovedBinaryImageUnit : IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`setImageData`](#setimagedata) | Sets the image data of the texture removed binary image. |
| [`getImageData`](#getimagedata) | Returns the image data of the texture removed binary image. |

### setImageData

Set the image data of the texture removed binary image.

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

`imageData`: A `DSImageData` object as the image data of the texture removed binary image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getImageData

Get the image data of the texture removed binary image.

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

The image data of the texture removed binary image.
