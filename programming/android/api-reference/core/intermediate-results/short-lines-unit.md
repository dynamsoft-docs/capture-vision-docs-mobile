---
layout: default-layout
title: ShortLinesUnit - Dynamsoft Core Module Android Edition API Reference
description: The class ShortLinesUnit of Dynamsoft Core Module represents a unit that contains the information of the detected short lines.
keywords: short lines unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ShortLinesUnit

The `ShortLinesUnit` class represents a unit that contains the information of the detected short lines.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class ShortLinesUnit extends IntermediateResultUnit
```

## Methods

| Methods | Desctiption |
| ------- | ----------- |
| [`getShortLines`](#getshortlines) | Gets the array of `LineSegment` as short lines. |
| [`getCount`](#getcount) | Gets the number of short lines. |
| [`getShortLine`](#getshortline) | Gets the short line at the specified index. |
| [`removeAllShortLines`](#removeallshortlines) | Removes all short lines. |
| [`removeShortLine`](#removeshortline) | Removes the short line at the specified index. |
| [`addShortLine`](#addshortline) | Adds the specified short line. |
| [`setShortLine`](#setshortline) | Sets the short line at the specified index. |

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

### getShortLines

Gets the array of `LineSegment` as short lines.

```java
LineSegment[] getShortLines()
```

**Return Value**

The array of `LineSegment` as short lines.

### getCount

Gets the number of short lines.

```java
int getCount()
```

**Return Value**

The number of short lines.

### getShortLine

Gets the short line at the specified index.

```java
LineSegment getShortLine(int index)
```

**Parameters**

`index`: The index of the short line.

**Return Value**

The short line at the specified index.

### removeAllShortLines

Removes all short lines.

```java
void removeAllShortLines()
```

### removeShortLine

Removes the short line at the specified index.

```java
int removeShortLine(int index)
```

**Parameters**

`index`: The index of the short line.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addShortLine

Adds the specified short line.

```java
int addShortLine(LineSegment line, Matrix matrixToOriginalImage)
```

**Parameters**

`line`: The short line to be added.

`matrixToOriginalImage`: The matrix to convert the coordinates of the short line to the original image coordinates.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setShortLine

Sets the short line at the specified index.

```java
int setShortLine(int index, LineSegment line,  Matrix matrixToOriginalImage)
```

**Parameters**

`index`: The index of the short line.

`line`: The short line to be set.

`matrixToOriginalImage`: The matrix to convert the coordinates of the short line to the original image coordinates.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
