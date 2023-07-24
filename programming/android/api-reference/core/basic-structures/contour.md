---
layout: default-layout
Title: Contour - Dynamsoft Core Module Android Edition API Reference
Description: The class Contour of Dynamsoft Core Module represents a contour in 2D space, which contains an array of CPoint objects, representing the vertices of the contour.
Keywords: contour, 2D space, CPoint, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Contour

The `Contour` class represents a contour in 2D space, which contains an array of CPoint objects, representing the vertices of the contour.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures
*Assembly:* DynamsoftCore.aar

```java
class Contour
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *NSArray \** | An array of `android.graphics.Point` that includes all vertices of the contour. |

### points

An array of `android.graphics.Point` that includes all vertices of the contour.

```java
Point[] points;
```
