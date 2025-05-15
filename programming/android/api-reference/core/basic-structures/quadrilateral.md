---
layout: default-layout
title: Quadrilateral - Dynamsoft Core Module Android Edition API Reference
description: The class Quadrilateral of Dynamsoft Core Module represents a quadrilateral shape in 2D space, which contains an array of four points, representing the vertices of the quadrilateral.
keywords: quadrilateral, shape, 2D space, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Quadrilateral

The `Quadrilateral` class represents a quadrilateral shape in 2D space, which contains an array of four points, representing the vertices of the quadrilateral.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
class Quadrilateral
```

## Methods & Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *android.graphics.Point[]* | Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex. |
| [`id`](#id) | *int* | The ID of the quadrilateral. |

| Method | Description |
| ------ | ----------- |
| [`contains`](#contains) | Check whether the input point is contained by the quadrilateral. |
| [`getBoundingRect`](#getboundingrect) | Get the bounding rectangle of the quadrilateral. |
| [`getArea`](#getarea) | Get the area of the quadrilateral. |

### points

Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex.

```java
Point[] points;
```

### id

The ID of the quadrilateral.

```java
int id;
```

### contains

Check whether the input point is contained by the quadrilateral.

```java
boolean contains(Point point);
```

**Parameters**

`[in] point`: Input a point.

**Return Value**

A boolean value that indicates whether the point is contained by the quadrilateral.

### getBoundingRect

Get the bounding rectangle of the quadrilateral.

```java
Rect getBoundingRect();
```

**Return Value**

The bounding rectangle of the quadrilateral.

### getArea

Get the area of the quadrilateral.

```java
int getArea();
```

**Return Value**

The area of the quadrilateral.
