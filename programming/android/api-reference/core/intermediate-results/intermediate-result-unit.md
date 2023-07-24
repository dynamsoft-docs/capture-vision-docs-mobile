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
| [`gethashId`](#gethashid) | The hash ID of the unit. |
| [`getSourceImageHashId`](#getsourceimagehashid) | The hash ID of the source image. You can use this ID to get the source image via `IntermediateResultManager` class. |
| [`getSourceImageTag`](#getsourceimagetag) | The image tag of the source image. |
| [`getType`](#gettype) | The type of the intermediate result unit. |
| [`getLocalToSourceImageTransformMatrix`](#getlocaltosourceimagetransformmatrix) | The transformation matrix from local to source image coordinates. |
| [`getRotationTransformMatrix`](#getrotationtransformmatrix) | The rotation transformation matrix of the original image relative to the rotated image. |

### getHashId

The hash ID of the unit.

```java
String getHashId();
```

### getSourceImageHashId

The hash ID of the source image. You can use this ID to get the source image via `IntermediateResultManager` class.

```java
String getSourceImageHashId();
```

### getSourceImageTag

The image tag of the source image.

```java
ImageTag getSourceImageTag();
```

### getType

The type of the intermediate result unit.

```java
long getType();
```

### getLocalToSourceImageTransformMatrix

The transformation matrix from local to source image coordinates.

```java
Matrix getLocalToSourceImageTransformMatrix();
```

### getRotationTransformMatrix

The rotation transformation matrix of the original image relative to the rotated image.

```java
Matrix getRotationTransformMatrix();
```

### clone

Creates a copy of the intermediate result unit.

```java
IntermediateResultUnit clone();
```

**Return Value**

A copy of the intermediate result unit.
