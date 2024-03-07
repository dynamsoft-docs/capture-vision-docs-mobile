---
layout: default-layout
title: DSGrayscaleImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSGrayscaleImageUnit of Dynamsoft Core Module represents a unit that contains a grayscale image. It is derived from the DSIntermediateResultUnit class.
keywords: grayscale image unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSGrayscaleImageUnit

The `DSGrayscaleImageUnit` class represents a unit that contains a grayscale image. It is derived from the `DSIntermediateResultUnit` class.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSGrayscaleImageUnit: DSIntermediateResultUnit
```
2. 
```swift
class GrayscaleImageUnit: IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the grayscale image. |

### imageData

A `DSImageData` object as the image data of the grayscale image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, strong, nullable) DSImageData *imageData;
```
2. 
```swift
var imageData: ImageData? { get set }
```
