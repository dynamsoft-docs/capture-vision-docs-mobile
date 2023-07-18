---
layout: default-layout
Title: DSContour - Dynamsoft Core Module Android Edition API Reference
Description: The class DSContour of Dynamsoft Core Module represents a contour in 2D space, which contains an array of CPoint objects, representing the vertices of the contour.
Keywords: contour, 2D space, CPoint, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSContour

The `DSContour` class represents a contour in 2D space, which contains an array of CPoint objects, representing the vertices of the contour.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class Contour
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`points`](#points) | *NSArray \** | An array includes all vertices of the contour. |

### points

An array includes all vertices of the contour.

```java
var points: [CPoint] { get set }
```
