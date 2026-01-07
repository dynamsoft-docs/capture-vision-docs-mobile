---
layout: default-layout
title: LineSegment - Dynamsoft Capture Vision Android Edition API Reference
description: The class LineSegment of Dynamsoft Capture Vision Android represents a line segment in 2D space, which contains the start point and end point of the line segment.
keywords: line segment, 2D, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LineSegment

The `LineSegment` class represents a line segment in 2D space, which contains the start point and end point of the line segment.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class LineSegment
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`startPoint`](#startpoint) | *android.graphics.Point* | The starting point of the line segment. |
| [`endPoint`](#endpoint) | *android.graphics.Point* | The ending point of the line segment. |
| [`id`](#id) | *int* | The ID of the line segment. |

| Method | Description |
| ------ | ----------- |
| [`LineSegment`](#linesegment-1) | The constructor. |
| [`LineSegment(startPoint,endPoint)`](#linesegmentstartpointendpoint) | Constructs a line segment from the start point and end point. |
| [`LineSegment(startPoint,endPoint,id)`](#linesegmentstartpointendpointid) | Constructs a line segment from the start point, end point, and ID. |
| [`transformByMatrix`](#transformbymatrix) | Transforms the coordinates of the line segment by a transformation matrix. |

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

### id

The ID of the line segment.

```java
int id;
```

### LineSegment

The constructor.

```java
LineSegment();
```

### LineSegment(startPoint,endPoint)

Constructs a line segment from the start point and end point.

```java
LineSegment(Point startPoint,Point endPoint);
```

### LineSegment(startPoint,endPoint,id)

Constructs a line segment from the start point, end point, and ID.

```java
LineSegment(Point startPoint,Point endPoint,int id);
```

### transformByMatrix

Transforms the coordinates of the line segment by a transformation matrix.

```java
LineSegment transformByMatrix(Matrix matrix);
```
