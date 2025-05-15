---
layout: default-layout
title: IntermediateResultUnit - Dynamsoft Core Module Android Edition API Reference
description: The class IntermediateResultUnit of Dynamsoft Core Module represents an intermediate result unit used in image processing, which is an abstract base class with multiple subclasses.
keywords: intermediate result unit, image processing, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultUnit

The `IntermediateResultUnit` class represents an intermediate result unit used in image processing. It is an abstract base class with multiple subclasses, each representing a different type of unit such as pre-detected regions, localized barcodes, decoded barcodes, localized text lines, binary image, gray image, etc.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`clone`](#clone) | Creates a copy of the intermediate result unit. |
| [`gethashId`](#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. You can use this ID to get the original image via `IntermediateResultManager` class. |
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the image tag of the original image associated with this unit. |
| [`getType`](#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`EnumIntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=android). |
| [`getTransformMatrix`](#gettransformmatrix) | Gets the transformation matrix via [`EnumTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html). |
| [`replace`](#replace) | Replaces the old unit with the new unit. |

### clone

Creates a copy of the intermediate result unit.

```java
IntermediateResultUnit clone();
```

**Return Value**

A copy of the intermediate result unit.

### getHashId

Gets the hash ID of the unit.

```java
String getHashId();
```

**Return Value**

The hash ID of the unit.

### getOriginalImageHashId

Gets the hash ID of the original image. You can use this ID to get the original image via `IntermediateResultManager` class.

```java
String getOriginalImageHashId();
```

**Return Value**

The hash ID of the original image.

### getOriginalImageTag

Gets the image tag of the original image.

```java
ImageTag getOriginalImageTag();
```

**Return Value**

The image tag of the original image.

### getType

Gets the type of the intermediate result unit.

```java
long getType();
```

**Return Value**

The type of the intermediate result unit.

### getTransformMatrix

Gets the transformation matrix via [`EnumTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html).

```java
Matrix getTransformMatrix(int matrixType);
```

**Parameters**

`[in] matrixType`: The transform matrix type.

**Return Value**

The corresponding transformation matrices are as follows:

- local image to original image
- original image to local image
- rotated image to original image
- original image to rotated image

### replace

Replaces the old unit with the new unit.

```java
int replace(IntermediateResultUnit oldUnit);
```

**Parameters**

`[in] oldUnit`: The old unit to be replaced.
