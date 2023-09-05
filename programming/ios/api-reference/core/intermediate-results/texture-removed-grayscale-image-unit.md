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

The `DSTextureRemovedGrayscaleImageUnit` class represents a unit that contains a texture-removed grayscale image. It is derived from the `DSIntermediateResultUnit` class.

## Definition

*Assembly:* DynamsoftCore.framework

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

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the texture-removed grayscale image. |

### imageData

A `DSImageData` object as the image data of the texture-removed grayscale image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong, nullable) DSImageData *imageData;
```
2. 
```swift
var imageData: ImageData? { get set }
```
