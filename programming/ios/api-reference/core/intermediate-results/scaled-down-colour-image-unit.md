---
layout: default-layout
title: DSScaledDownColourImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSScaledDownColourImageUnit of Dynamsoft Core Module represents a unit that contains a down-scaled colour image.
keywords: scaled down colour image unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSScaledDownColourImageUnit

The `DSScaledDownColourImageUnit` class represents a unit that contains a down-scaled colour image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSScaledDownColourImageUnit : DSIntermediateResultUnit
```
2. 
```swift
class ScaledDownColourImageUnit : DSIntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`setImageData`](#setimagedata) | Sets the image data of the down-scaled colour image. |
| [`getImageData`](#getimagedata) | Returns the image data of the down-scaled colour image. |

### setImageData

Set the image data of the down-scaled colour image.

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

Get the image data of the down-scaled colour image.

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

The image data of the down-scaled colour image.
