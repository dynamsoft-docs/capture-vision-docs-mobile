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

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class Quadrilateral
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *android.graphics.Point[]* | Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex. |
| [`id`](#id) | *int* | The ID of the quadrilateral. |

| Method | Description |
| ------ | ----------- |
| [`Quadrilateral`](#quadrilateral-1) | The constructor. |
| [`Quadrilateral(quad)`](#quadrilateralquad) | Constructs a quadrilateral from another quadrilateral. |
| [`Quadrilateral(point1,point2,point3,point4)`](#quadrilateralpoint1point2point3point4) | Constructs a quadrilateral from four points. |
| [`Quadrilateral(point1,point2,point3,point4,id)`](#quadrilateralpoint1point2point3point4id) | Constructs a quadrilateral from four points and an ID. |
| [`fromJson`](#fromjson) | Constructs a quadrilateral from a JSON string. |
| [`transformByMatrix`](#transformbymatrix) | Transforms the coordinates of the quadrilateral by a transformation matrix. |
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

### Quadrilateral

The constructor.

```java
Quadrilateral();
```

### Quadrilateral(quad)

Constructs a quadrilateral from another quadrilateral.

```java
Quadrilateral(Quadrilateral quad);
```

### Quadrilateral(point1,point2,point3,point4)

Constructs a quadrilateral from four points.

```java
Quadrilateral(Point point1,Point point2,Point point3,Point point4);
```

### Quadrilateral(point1,point2,point3,point4,id)

Constructs a quadrilateral from four points and an ID.

```java
Quadrilateral(Point point1,Point point2,Point point3,Point point4,int id);
```

### fromJson

Constructs a quadrilateral from a JSON string.

```java

Quadrilateral fromJson(String jsonString);
```

**Return Value**

The constructed quadrilateral.

### transformByMatrix

Transforms the coordinates of the quadrilateral by a transformation matrix.

```java
Quadrilateral transformByMatrix(Matrix matrix);
```

**Parameters**

`matrix`: The transformation matrix.

**Return Value**

The transformed quadrilateral.

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
