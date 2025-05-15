---
layout: default-layout
title: EnhancedGrayscaleImageUnit - Dynamsoft Core Module Android Edition API Reference
description: The class EnhancedGrayscaleImageUnit of Dynamsoft Core Module represents a unit that contains a grayscale enhanced image.
keywords: enhanced grayscale image unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# EnhancedGrayscaleImageUnit

The `EnhancedGrayscaleImageUnit` class represents a unit that contains a grayscale enhanced image.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class EnhancedGrayscaleImageUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getImageData`](#getimagedata) | Gets the image data for the enhanced grayscale image. |
| [`setImageData`](#setimagedata) | Sets the image data for the enhanced grayscale image. |

## Inherited Methods

The following methods are inherited from class [`IntermediateResultUnit`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`clone`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`gethashId`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image. You can use this ID to get the original image via `IntermediateResultManager` class. |
| [`getOriginalImageTag`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the image tag of the original image associated with this unit. |
| [`getType`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`EnumIntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=android). |
| [`getTransformMatrix`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`EnumTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html). |
| [`replace`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the old unit with the new unit. |

### getImageData

Gets the image data for the enhanced grayscale image.

```java
ImageData getImageData();
```

**Return Value**

The `ImageData` object as the image data of the enhanced grayscale image.

### setImageData

Sets the image data for the enhanced grayscale image.

```java
int setImageData(ImageData imageData);
```

**Parameter**

`imageData`: The `ImageData` object as the image data of the enhanced grayscale image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
