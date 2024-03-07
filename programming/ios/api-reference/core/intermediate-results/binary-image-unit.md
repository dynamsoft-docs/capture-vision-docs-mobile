---
layout: default-layout
title: DSBinaryImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSBinaryImageUnit of Dynamsoft Core Module represents a unit that contains a binary image.
keywords: binary image, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSBinaryImageUnit

The `DSBinaryImageUnit` class represents a unit that contains a binary image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSBinaryImageUnit: DSIntermediateResultUnit
```
2. 
```swift
class BinaryImageUnit : IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`setImageData`](#setimagedata) | Sets the image data of the binary image. |
| [`getImageData`](#getimagedata) | Returns the image data of the binary image. |

### setImageData

Set the image data of the binary image.

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

`imageData`: A `DSImageData` object as the image data of the binary image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getImageData

Get the image data of the binary image.

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

The image data of the binary image.
