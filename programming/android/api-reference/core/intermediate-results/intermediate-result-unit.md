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
| [`getSourceImageHashId`](#getsourceimagehashid) | Gets the hash ID of the source image. You can use this ID to get the source image via `IntermediateResultManager` class. |
| [`getSourceImageTag`](#getsourceimagetag) | Gets the image tag of the source image. |
| [`getType`](#gettype) | Gets the type of the intermediate result unit. |
| [`getLocalToSourceImageTransformMatrix`](#getlocaltosourceimagetransformmatrix) | Gets the transformation matrix from local to source image coordinates. |
| [`getRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the rotation transformation matrix of the original image relative to the rotated image. |

### getHashId

Gets the hash ID of the unit.

```java
String getHashId();
```

**Return Value**

The hash ID of the unit.

### getSourceImageHashId

Gets the hash ID of the source image. You can use this ID to get the source image via `IntermediateResultManager` class.

```java
String getSourceImageHashId();
```

**Return Value**

The hash ID of the source image.

### getSourceImageTag

Gets the image tag of the source image.

```java
ImageTag getSourceImageTag();
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

### getLocalToSourceImageTransformMatrix

Gets the transformation matrix from local to source image coordinates.

```java
Matrix getLocalToSourceImageTransformMatrix();
```

**Return Value**

The transformation matrix from local to source image coordinates.

### getRotationTransformMatrix

Gets the rotation transformation matrix of the original image relative to the rotated image.

```java
Matrix getRotationTransformMatrix();
```

**Return Value**

The rotation transformation matrix of the original image relative to the rotated image.

### clone

Creates a copy of the intermediate result unit.

```java
IntermediateResultUnit clone();
```

**Return Value**

A copy of the intermediate result unit.
