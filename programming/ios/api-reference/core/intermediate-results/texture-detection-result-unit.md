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

## Inherited Methods

The following methods are inherited from class [`IntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`getHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image associated with this unit. |
| [`getOriginalImageTag`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the image tag of the original image. |
| [`getType`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`IntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=objc,swift). |
| [`getTransformMatrix`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`DSTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html). |
| [`clone`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`replace`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the content of the intermediate result unit. |

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
