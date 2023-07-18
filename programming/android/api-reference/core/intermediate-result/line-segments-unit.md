---
layout: default-layout
Title: DSLineSegmentsUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class DSLineSegmentsUnit of Dynamsoft Core Module represents a collection of line segments in 2D space.
Keywords: line segments, 2D space, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLineSegmentsUnit

The `DSLineSegmentsUnit` class represents a collection of line segments in 2D space. It is a derived class of `DSIntermediateResultUnit`.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class LineSegmentsUnit extends IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`lineSegments`](#linesegments) | *NSArray<DSLineSegment*>* \** | An array of `DSLineSegment`. |

### lineSegments

An array of `DSLineSegment`.

```java
var lineSegments: [DSLineSegment]? { get set }
```
