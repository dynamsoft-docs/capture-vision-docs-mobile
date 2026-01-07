---
layout: default-layout
title: TextureDetectionResultUnit - Dynamsoft Capture Vision Android Edition API Reference
description: The class TextureDetectionResultUnit of Dynamsoft Capture Vision Android represents an intermediate result unit for texture detection, which contains the x-direction spacing and y-direction spacing of the texture stripes.
keywords: texture detection, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextureDetectionResultUnit

The `TextureDetectionResultUnit` class extends the `IntermediateResultUnit` class and represents a texture-detection result unit. This class captures the results of texture analysis, specifically the spacing of texture patterns in both the x and y directions.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class TextureDetectionResultUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getXSpacing`](#getxspacing) | Gets the X-direction spacing of the texture stripes. |
| [`getYSpacing`](#getyspacing) | Gets the Y-direction spacing of the texture stripes. |
| [`setXSpacing`](#setxspacing) | Sets the X-direction spacing of the texture stripes. |
| [`setYSpacing`](#setyspacing) | Sets the Y-direction spacing of the texture stripes. |

## Inherited Methods

The following methods are inherited from class [`IntermediateResultUnit`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`clone`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`gethashId`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image. You can use this ID to get the original image via `IntermediateResultManager` class. |
| [`getOriginalImageTag`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the image tag of the original image associated with this unit. |
| [`getType`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`EnumIntermediateResultUnitType`]({{ site.dcv_android_api }}core/enum/intermediate-result-unit-type.html?lang=android). |
| [`getTransformMatrix`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`EnumTransformMatrixType`]({{ site.dcv_android_api }}core/enum/transform-matrix-type.html). |
| [`replace`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the old unit with the new unit. |

### getXSpacing

Gets the X-direction spacing of the texture stripes.

```java
int getXSpacing()
```

**Return Value**

The X-direction spacing of the texture stripes. This value represents the detected horizontal distance in pixels between consecutive texture patterns, providing an indication of the texture's density and orientation within the image.

### getYSpacing

Gets the Y-direction spacing of the texture stripes.

```java
int getYSpacing()
```

**Return Value**

The Y-direction spacing of the texture stripes. This value represents the spacing between texture stripes in the y-direction. Similar to `xSpacing`, this value measures the vertical distance between texture patterns. It offers insights into the vertical density and alignment of the texture within the image, contributing to the understanding of the texture's characteristics and spatial distribution.

### setXSpacing

Sets the X-direction spacing of the texture stripes.

```java
void setXSpacing(int xSpacing)
```

**Parameter**

`[in] xSpacing`: The X-direction spacing of the texture stripes.

### setYSpacing

Sets the Y-direction spacing of the texture stripes.

```java
void setYSpacing(int ySpacing)
```

**Parameter**

`[in] ySpacing`: The Y-direction spacing of the texture stripes.
