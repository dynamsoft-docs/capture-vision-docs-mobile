---
layout: default-layout
title: Corner - Dynamsoft Core Module Android Edition API Reference
description: The class Corner of Dynamsoft Core Module represents a detected corner, which consists of an intersection and two lines.
keywords: corner, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Corner

The `Corner` class represents a detected corner, which consists of an intersection point and two lines of the corner.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
class Corner
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`type`](#type) | *[EnumCornerType]({{ site.dcv_enumerations }}core/corner-type.html?lang=android)* | The type of the corner. The types are availabled as normal-intersected, T-intersected, cross-intersected, not-intersected. |
| [`intersection`](#intersection) | *android.graphics.Point* | The coordinate of the intersection point of the corner. |
| [`line1`](#line1) | *[LineSegment](line-segment.md)* |One of the lines of the corner. Defined in LineSegment. |
| [`line2`](#line2) | *[LineSegment](line-segment.md)* |One of the lines of the corner. Defined in LineSegment. |

### type

The type of the corner. The types are availabled as normal-intersected, T-intersected, cross-intersected, not-intersected.

```java
EnumCornerType type;
```

### intersection

The coordinate of the intersection point of the corner.

```java
Point intersection;
```

### line1

One of the lines of the corner. Defined in `LineSegment`.

```java
LineSegment line1;
```

### line2

One of the lines of the corner. Defined in `LineSegment`.

```java
LineSegment line2;
```
