---
layout: default-layout
title: TextureRemovedBinaryImageUnit - Dynamsoft Core Module Android Edition API Reference
description: The class TextureRemovedBinaryImageUnit of Dynamsoft Core Module represents a unit that contains a texture-removed binary image.
keywords: texture-removed binary image, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextureRemovedBinaryImageUnit

The `TextureRemovedBinaryImageUnit` class extends the `IntermediateResultUnit` class and represents a texture-removed binary image unit.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class TextureRemovedBinaryImageUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getImageData`](#getimagedata) | Gets the `ImageData` for the texture-removed binary image. |
| [`setImageData`](#setimagedata) | Sets the `ImageData` for the texture-removed binary image. |

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

### getImageData

Gets the `ImageData` object as the image data of the texture-removed binary image.

```java
ImageData getImageData();
```

**Return Value**

The `ImageData` object as the image data of the texture-removed binary  image.

### setImageData

Sets the `ImageData` object as the image data of the texture-removed binary image.

```java
int setImageData(ImageData imageData);
```

**Parameter**

`imageData`: The `ImageData` object as the image data of the texture-removed binary image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
