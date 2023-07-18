---
layout: default-layout
Title: DSCorner - Dynamsoft Core Module Android Edition API Reference
Description: The class DSCorner of Dynamsoft Core Module represents a detected corner, which consists of an intersection and two lines.
Keywords: corner, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCorner

The `DSCorner` class represents a detected corner, which consists of an intersection point and two lines of the corner.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class Corner
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`type`](#type) | *DSCornerType* | The type of the corner. The types are availabled as normal-intersected, T-intersected, cross-intersected, not-intersected. |
| [`intersection`](#intersection) | *CGPoint* | The coordinate of the intersection point of the corner. |
| [`line1`](#line1) | *DSLineSegment \** |One of the lines of the corner. Defined in DSLineSegment. |
| [`line2`](#line2) | *DSLineSegment \** |One of the lines of the corner. Defined in DSLineSegment. |

### type

The type of the corner. The types are availabled as normal-intersected, T-intersected, cross-intersected, not-intersected.

```java
var type: DSCornerType { get set }
```

### intersection

The coordinate of the intersection point of the corner.

```java
var intersection: CGPoint { get set }
```

### line1

One of the lines of the corner. Defined in DSLineSegment.

```java
var line1: DSLineSegment? { get set }
```

### line2

One of the lines of the corner. Defined in DSLineSegment.

```java
var line2: DSLineSegment? { get set }
```
