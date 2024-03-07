---
layout: default-layout
title: LineSegmentsUnit - Dynamsoft Core Module Android Edition API Reference
description: The class LineSegmentsUnit of Dynamsoft Core Module represents a collection of line segments in 2D space.
keywords: line segments, 2D space, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LineSegmentsUnit

The `LineSegmentsUnit` class represents a collection of line segments in 2D space. It is a derived class of `IntermediateResultUnit`.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class LineSegmentsUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getLineSegments`](#getlinesegments) | Gets the array of [`LineSegment`](../basic-structures/line-segment.html). |
| [`getCount`](#getcount) | Gets the number of line segments. |
| [`getLineSegment`](#getlinesegment) | Gets the [`LineSegment`](../basic-structures/line-segment.html) at the specified index. |
| [`removeAllLineSegments`](#removealllinesegments) | Removes all line segments. |
| [`removeLineSegment`](#removelinesegment) | Removes the line segment at the specified index. |
| [`addLineSegment`](#addlinesegment) | Adds a line segment. |
| [`setLineSegment`](#setlinesegment) | Sets the line segment at the specified index. |

### getLineSegments

Gets the array of [`LineSegment`](../basic-structures/line-segment.html).

```java
LineSegment[] getLineSegments();
```

**Return Value**

The array of [`LineSegment`](../basic-structures/line-segment.html).

### getCount

Gets the number of line segments.

```java
int getCount();
```

**Return Value**

The number of line segments.

### getLineSegment

Gets the [`LineSegment`](../basic-structures/line-segment.html) at the specified index.

```java
LineSegment getLineSegment(int index);
```

**Return Value**

The [`LineSegment`](../basic-structures/line-segment.html) at the specified index.

### removeAllLineSegments

Removes all line segments.

```java
void removeAllLineSegments();
```

### removeLineSegment

Removes the line segment at the specified index.

```java
int removeLineSegment(int index);
```

**Parameters**

`[in] index`: The index of the line segment to remove.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addLineSegment

Adds a line segment.

```java
int addLineSegment(LineSegment line, Matrix matrixToOriginalImage);
```

**Parameters**

`[in] line`: The line segment to add.

`[in] matrixToOriginalImage`: The transformation matrix from the line segment to the original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setLineSegment

Sets the line segment at the specified index.

```java
int setLineSegment(int index, LineSegment line,  Matrix matrixToOriginalImage);
```

**Parameters**

`[in] index`: The index of the line segment to set.

`[in] line`: The line segment to set.

`[in] matrixToOriginalImage`: The transformation matrix from the line segment to the original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
