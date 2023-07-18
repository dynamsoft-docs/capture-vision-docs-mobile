---
layout: default-layout
Title: DSIntermediateResultUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class DSIntermediateResultUnit of Dynamsoft Core Module represents an intermediate result unit used in image processing, which is an abstract base class with multiple subclasses.
Keywords: intermediate result unit, image processing, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIntermediateResultUnit

The `DSIntermediateResultUnit` class represents an intermediate result unit used in image processing. It is an abstract base class with multiple subclasses, each representing a different type of unit such as pre-detected regions, localized barcodes, decoded barcodes, localized text lines, binary image, gray image, etc.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`hashId`](#hashid) | *NSString \** | The hash ID of the unit. |
| [`sourceImageHashId`](#sourceimagehashid) | *NSString \** | The hash ID of the source image. You can use this ID to get the source image via `IntermediateResultManager` class. |
| [`sourceImageTag`](#sourceimagetag) | *DSImageTag \** | The image tag of the source image. |
| [`type`](#type) | *DSIntermediateResultUnitType* | The type of the intermediate result unit. |
| [`localToSourceImageTransformMatrix`](#localtosourceimagetransformmatrix) | *CGAffineTransform* | The transformation matrix from local to source image coordinates. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image. |

## Methods

| Method | Description |
|------- |-------------|
| [`clone`](#clone) | Creates a copy of the intermediate result unit. |

### hashId

The hash ID of the unit.

```java
var hashId: String? { get }
```

### sourceImageHashId

The hash ID of the source image. You can use this ID to get the source image via `IntermediateResultManager` class.

```java
var sourceImageHashId: String? { get }
```

### sourceImageTag

The image tag of the source image.

```java
var sourceImageTag: ImageTag? { get }
```

### type

The type of the intermediate result unit.

```java
var type: EnumIntermediateResultUnitType { get }
```

### localToSourceImageTransformMatrix

The transformation matrix from local to source image coordinates.

```java
var localToSourceImageTransformMatrix: CGAffineTransform { get }
```

### rotationTransformMatrix

The rotation transformation matrix of the original image relative to the rotated image.

```java
var rotationTransformMatrix: CGAffineTransform { get }
```

### clone

Creates a copy of the intermediate result unit.

```java
func clone() -> IntermediateResultUnit
```

**Return Value**

A copy of the intermediate result unit.
