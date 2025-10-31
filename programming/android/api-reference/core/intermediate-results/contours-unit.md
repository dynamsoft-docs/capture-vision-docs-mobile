---
layout: default-layout
title: ContoursUnit - Dynamsoft Core Module Android Edition API Reference
description: The class ContoursUnit of Dynamsoft Core Module represents a unit that contains contours as intermediate results.
keywords: contours unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ContoursUnit

The `ContoursUnit` class represents a unit that contains contours as intermediate results. It is derived from the `IntermediateResultUnit` class.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class ContoursUnit: IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getContours`](#getcontours) | Gets the contour array of the unit. |
| [`setContours`](#setcontours) | Sets the contour array for the unit. |
| [`getHierarchies`](#gethierarchies) | Gets the contour hierarchies as an array of `Vector4` objects. |

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

### getContours

Gets the contour array of the unit.

```java
@Nullable
Contour[] getContours()
```

**Return Value**

The array of `Contour` objects.

### setContours

Sets the contour array for the unit.

```java
int setContours(Contour[] contours, Vector4[] hierarchies, Matrix matrixToOriginalImage);
```

**Parameters**

`contours`: The array of `Contour` objects.

`hierarchies`: The contour hierarchies as an array of `Vector4` objects.

`matrixToOriginalImage`: The transformation matrix of the original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getHierarchies

Gets the contour hierarchies as an array of `Vector4` objects.

```java
@Nullable
Vector4[] getHierarchies()
```

**Return Value**

The contour hierarchies as an array of `Vector4` objects.
