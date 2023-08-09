---
layout: default-layout
Title: IntermediateResultUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class IntermediateResultUnit of Dynamsoft Core Module represents an intermediate result unit used in image processing, which is an abstract base class with multiple subclasses.
Keywords: intermediate result unit, image processing, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultUnit

The `IntermediateResultUnit` class represents an intermediate result unit used in image processing. It is an abstract base class with multiple subclasses, each representing a different type of unit such as pre-detected regions, localized barcodes, decoded barcodes, localized text lines, binary image, gray image, etc.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class IntermediateResultUnit
```

## Methods

| Method | Description |
|------- |-------------|
| [`clone`](#clone) | Creates a copy of the intermediate result unit. |
| [`gethashId`](#gethashid) | Gets the hash ID of the unit. |
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the source image. You can use this ID to get the source image via `IntermediateResultManager` class. |
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the image tag of the source image. |
| [`getType`](#gettype) | Gets the type of the intermediate result unit. |
| [`getTransformMatrix`](#gettransformmatrix) | Gets the transformation matrix via [`EnumTransformMatrixType`]({{site.enums}}/core/transform-matrix-type.html). |

### getHashId

Gets the hash ID of the unit.

```java
String getHashId();
```

**Return Value**

The hash ID of the unit.

### getOriginalImageHashId

Gets the hash ID of the source image. You can use this ID to get the source image via `IntermediateResultManager` class.

```java
String getOriginalImageHashId();
```

**Return Value**

The hash ID of the source image.

### getOriginalImageTag

Gets the image tag of the source image.

```java
ImageTag getOriginalImageTag();
```

**Return Value**

The image tag of the source image.

### getType

Gets the type of the intermediate result unit.

```java
long getType();
```

**Return Value**

The type of the intermediate result unit.

### getTransformMatrix

Gets the transformation matrix via [`EnumTransformMatrixType`]({{site.enums}}/core/transform-matrix-type.html).

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

### clone

Creates a copy of the intermediate result unit.

```java
IntermediateResultUnit clone();
```

**Return Value**

A copy of the intermediate result unit.