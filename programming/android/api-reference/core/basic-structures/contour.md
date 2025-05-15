---
layout: default-layout
title: Contour - Dynamsoft Core Module Android Edition API Reference
description: The class Contour of Dynamsoft Core Module represents a contour in 2D space, which contains an array of CPoint objects, representing the vertices of the contour.
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

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *android.graphics.Point[]* | An array of `Point` objects defining the vertices of the contour. |

### points

An array of `android.graphics.Point` objects defining the vertices of the contour.

```java
Point[] points;
```
