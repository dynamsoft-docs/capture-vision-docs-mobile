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

### getLineSegments

Gets the array of [`LineSegment`](../basic-structures/line-segment.html).

```java
LineSegment[] getLineSegments();
```

**Return Value**

The array of [`LineSegment`](../basic-structures/line-segment.html).
