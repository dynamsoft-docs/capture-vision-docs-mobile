---
layout: default-layout
title: Edge - Dynamsoft Capture Vision Android Edition API Reference
description: The class Edge of Dynamsoft Capture Vision Android represents an edge of candidate quadrilaterals, which consists of two corners.
keywords: edge, quadrilateral, corner, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Edge

The `Edge` class represents an edge defined by two `Corners`.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class Edge
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`startCorner`](#startcorner) | *[Corner](corner.md)* | The starting corner of the edge. |
| [`endCorner`](#endcorner) | *[Corner](corner.md)* | The ending corner of the edge. |

| Method | Description |
|------- |-------------|
| [`Edge`](#edge-1) | The default constructor. |
| [`Edge(startCorner,endCorner)`](#edgestartcornerendcorner) | Constructs a corner from the type, intersection, and lines. |
| [`transformByMatrix`](#transformbymatrix) | Transforms the coordinates of the corner by a transformation matrix. |

### startCorner

The starting corner of the edge.

```java
Corner startCorner;
```

### endCorner

The ending corner of the edge.

```java
Corner endCorner;
```

### Edge

```java
Edge();
```

### Edge(startCorner,endCorner)

```java
Edge(Corner startCorner, Corner endCorner);
```

### transformByMatrix

```java
Edge transformByMatrix(Matrix matrix);
```

**Parameters**

`matrix`: The transformation matrix.

**Return Value**

The transformed edge.
