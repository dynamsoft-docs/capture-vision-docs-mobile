---
layout: default-layout
title: LineSegment - Dynamsoft Core Module Android Edition API Reference
description: The class LineSegment of Dynamsoft Core Module represents a line segment in 2D space, which contains the start point and end point of the line segment.
keywords: line segment, 2D, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LineSegment

The `LineSegment` class represents a line segment in 2D space, which contains the start point and end point of the line segment.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
class LineSegment
```

## Attribute Summaries

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`startPoint`](#startpoint) | *android.graphics.Point* | The starting point of the line segment. |
| [`endPoint`](#endpoint) | *android.graphics.Point* | The ending point of the line segment. |

## Method Summaries

| Method | Description |
| ------ | ----------- |
| [`LineSegment`](#linesegment-1) | The constructor. |

## Attribute Details

### startPoint

The start point of the line segment.

```java
Point startPoint;
```

### endPoint

The end point of the line segment.

```java
Point endPoint;
```

## Method Details

### LineSegment

The constructor.

```java
LineSegment();
```
