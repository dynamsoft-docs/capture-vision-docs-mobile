---
layout: default-layout
title: DSTransformedGrayscaleImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSTransformedGrayscaleImageUnit of Dynamsoft Core Module represents a unit that contains a transformed grayscale image.
keywords: transformed grayscale image, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTransformedGrayscaleImageUnit

The `DSTransformedGrayscaleImageUnit` class represents a unit that contains a transformed grayscale image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSTransformedGrayscaleImageUnit: DSIntermediateResultUnit
```
2. 
```swift
class TransformedGrayscaleImageUnit : IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the transformed grayscale image. |

### imageData

A `DSImageData` object as the image data of the transformed grayscale image.

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
var imageData: DSImageData? { get set }
```
