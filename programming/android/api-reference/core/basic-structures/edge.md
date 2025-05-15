---
layout: default-layout
title: Edge - Dynamsoft Core Module Android Edition API Reference
description: The class Edge of Dynamsoft Core Module represents an edge of candidate quadrilaterals, which consists of two corners.
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

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`startCorner`](#startcorner) | *[Corner](corner.md)* | The starting corner of the edge. |
| [`endCorner`](#endcorner) | *[Corner](corner.md)* | The ending corner of the edge. |

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
