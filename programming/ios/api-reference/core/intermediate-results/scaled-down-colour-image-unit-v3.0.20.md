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
NS_SWIFT_NAME(ScaledDownColourImageUnit)
@interface DSScaledDownColourImageUnit : DSIntermediateResultUnit
```
2. 
```swift
class ScaledDownColourImageUnit : DSIntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the down-scaled colour image. |

### imageData

A `DSImageData` object as the image data of the down-scaled colour image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable) DSImageData *imageData
```
2. 
```swift
var imageData: DSImageData? { get set }
```
