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
| [`removeAllShortLines`](#removeshortlines) | Removes all short lines. |
| [`removeShortLine`](#removeshortline) | Removes the short line at the specified index. |
| [`addShortLine`](#addshortline) | Adds the specified short line. |
| [`setShortLine`](#setshortline) | Sets the short line at the specified index. |

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
