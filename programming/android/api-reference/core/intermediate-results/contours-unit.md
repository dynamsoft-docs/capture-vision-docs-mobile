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

*Assembly:* DynamsoftCore.aar

```java
class ContoursUnit: IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getContours`](#getcontours) | Gets the contour array of the unit. |
| [`setContours`](#setcontours) | Sets the contour array for the unit. |
| [`getHierarchies`](#gethierarchies) | Gets the contour hierarchies as an array of `Vector4` objects. |

public int setContours(Contour[] contours, Vector4[] hierarchies, Matrix matrixToOriginalImage);

### getContours

Gets the contour array of the unit.

```java
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
Vector4[] getHierarchies()
```

**Return Value**

The contour hierarchies as an array of `Vector4` objects.
