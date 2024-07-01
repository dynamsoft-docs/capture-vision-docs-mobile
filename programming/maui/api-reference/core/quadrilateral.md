---
layout: default-layout
title: Quadrilateral - Dynamsoft Capture Vision MAUI API Reference
description: The class Quadrilateral of DCV MAUI represents a quadrilateral shape in 2D space, which contains an array of four points, representing the vertices of the quadrilateral.
keywords: quadrilateral, shape, 2D space
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Quadrilateral

The `Quadrilateral` class represents a quadrilateral shape in 2D space, which contains an array of four points, representing the vertices of the quadrilateral.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
class Quadrilateral
```

## Methods & Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`Points`](#points) | *Microsoft.Maui.Graphics.Point[]* | Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex. |

| Method | Description |
| ------ | ----------- |
| [`Quadrilateral`](#quadrilateral-1) | The constructor. |
| [`Contains`](#contains) | Check whether the input point is contained by the quadrilateral. |
| [`GetBoundingRect`](#getboundingrect) | Get the bounding rectangle of the quadrilateral. |
| [`GetArea`](#getarea) | Get the area of the quadrilateral. |

### Points

Four vertexes in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex.

```csharp
Microsoft.Maui.Graphics.Point[] Points { get; }
```

### Quadrilateral

The constructor.

```csharp
Quadrilateral(Microsoft.Maui.Graphics.Point[] points);
```

### Contains

Check whether the input point is contained by the quadrilateral.

```csharp
bool Contains(Microsoft.Maui.Graphics.Point point);
```

**Parameters**

`[in] point`: Input a point.

**Return Value**

A boolean value that indicates whether the point is contained by the quadrilateral.

### GetBoundingRect

Get the bounding rectangle of the quadrilateral.

```csharp
Microsoft.Maui.Graphics.Rect GetBoundingRect();
```

**Return Value**

The bounding rectangle of the quadrilateral.

### GetArea

Get the area of the quadrilateral.

```csharp
int GetArea();
```

**Return Value**

The area of the quadrilateral.
