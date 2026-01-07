---
layout: default-layout
title: Contour - Dynamsoft Capture Vision Android Edition API Reference
description: The class Contour of Dynamsoft Capture Vision Android represents a contour in 2D space, which contains an array of CPoint objects, representing the vertices of the contour.
keywords: contour, 2D space, CPoint, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Contour

The `Contour` class represents a contour made up of multiple points.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class Contour
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *android.graphics.Point[]* | An array of `Point` objects defining the vertices of the contour. |

| Method | Description |
|------- |-------------|
| [`Contour`](#contour-1) | The default constructor. |
| [`Contour(Point[])`](#contourpoint-points) | Constructs a contour from an array of points. |
| [`transformByMatrix`](#transformbymatrix) | Transforms the coordinates of the contour by a transformation matrix. |

### points

An array of `android.graphics.Point` objects defining the vertices of the contour.

```java
Point[] points;
```

### Contour

The default constructor.

```java
Contour();
```

### Contour(Point[] points)

Constructs a contour from an array of points.

```java
Contour(Point[] points);
```

### transformByMatrix

```java
Contour transformByMatrix(Matrix matrix);
```

**Parameters**

`matrix`: The transformation matrix.

**Return Value**

The transformed contour.
