---
layout: default-layout
Title: DSEdge - Dynamsoft Core Module Android Edition API Reference
Description: The class DSEdge of Dynamsoft Core Module represents an edge of candidate quadrilaterals, which consists of two corners.
Keywords: edge, quadrilateral, corner, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSEdge

The `DSEdge` class represents an edge of candidate quadrilaterals, which consists of two corners.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class Edge
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`startCorner`](#startcorner) | *DSCorner \** | The start corner of the edge. |
| [`endCorner`](#endcorner) | *DSCorner \** | The end corner of the edge. |

### startCorner

The start corner of the edge.

```java
var startCorner: Corner? { get set }
```

### endCorner

The end corner of the edge.

```java
var endCorner: Corner? { get set }
```
