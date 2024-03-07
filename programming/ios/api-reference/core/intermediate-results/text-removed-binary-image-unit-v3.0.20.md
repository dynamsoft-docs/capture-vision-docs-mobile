---
layout: default-layout
title: DSTextRemovedBinaryImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSTextRemovedBinaryImageUnit of Dynamsoft Core Module represents a unit that contains a text-removed binary image.
keywords: text-removed binary image, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextRemovedBinaryImageUnit

The `DSTextRemovedBinaryImageUnit` class represents a unit that contains a text-removed binary image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSTextRemovedBinaryImageUnit : DSIntermediateResultUnit
```
2. 
```swift
class TextRemovedBinaryImageUnit : IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the text-removed binary image. |

### imageData

A `DSImageData` object as the image data of the text-removed binary image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable) DSImageData *imageData;
```
2. 
```swift
var imageData: ImageData? { get set }
```
