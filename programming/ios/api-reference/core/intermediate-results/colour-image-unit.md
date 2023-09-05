---
layout: default-layout
title: DSColourImageUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSColourImageUnit of Dynamsoft Core Module represents a unit that contains a colour image.
keywords: colour image unit, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSColourImageUnit

The `DSColourImageUnit` class represents a unit that contains a colour image.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSColourImageUnit: DSIntermediateResultUnit
```
2. 
```swift
class ColourImageUnit : DSIntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the binary image. |

### imageData

A `DSImageData` object as the image data of the binary image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable) DSImageData* imageData;
```
2. 
```swift
var imageData: DSImageData? { get set }
```
