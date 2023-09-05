---
layout: default-layout
title: DSTextureDetectionResultUnit - Dynamsoft Core Module iOS Edition API Reference
description: The class DSTextureDetectionResultUnit of Dynamsoft Core Module represents an intermediate result unit for texture detection, which contains the x-direction spacing and y-direction spacing of the texture stripes.
keywords: texture detection, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextureDetectionResultUnit

The `DSTextureDetectionResultUnit` class represents an intermediate result unit for texture detection, which contains the x-direction spacing and y-direction spacing of the texture stripes.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(TextureDetectionResultUnit)
@interface DSTextureDetectionResultUnit: DSIntermediateResultUnit
```
2. 
```swift
class TextureDetectionResultUnit : IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`xSpacing`](#xspacing) | *NSInteger* | X-direction spacing of the texture stripes. |
| [`ySpacing`](#yspacing) | *NSInteger* | Y-direction spacing of the texture stripes. |

### xSpacing

X-direction spacing of the texture stripes.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger xSpacing
```
2. 
```swift
var xSpacing: Int { get set }
```

### ySpacing

Y-direction spacing of the texture stripes.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger ySpacing
```
2. 
```swift
var ySpacing: Int { get set }
```
