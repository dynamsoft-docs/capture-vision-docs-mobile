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

The `Corner` class represents a corner, typically where two line segments meet

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class Corner
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`type`](#type) | *int* | The type of the corner. The types are availabled as normal-intersected, T-intersected, cross-intersected, not-intersected. |
| [`intersection`](#intersection) | *android.graphics.Point* | The coordinate of the intersection point of the corner. |
| [`line1`](#line1) | *[LineSegment](line-segment.md)* | One of the lines of the corner. Defined in LineSegment. |
| [`line2`](#line2) | *[LineSegment](line-segment.md)* | One of the lines of the corner. Defined in LineSegment. |

| Method | Description |
|------- |-------------|
| [`Corner`](#corner-1) | The default constructor. |
| [`Corner(type,insection,line1,line2)`](#cornertypeinsectionline1line2) | Constructs a corner from the type, intersection, and lines. |
| [`transformByMatrix`](#transformbymatrix) | Transforms the coordinates of the corner by a transformation matrix. |

### type

The type of the corner. The types are availabled as normal-intersected, T-intersected, cross-intersected, not-intersected.

```java
@EnumCornerType
int type;
```

Related APIs:

- [EnumCornerType]({{ site.dcv_android_api }}core/enum/corner-type.html?lang=android)

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

### Corner

The default constructor.

```java
Corner();
```

### Corner(type,insection,line1,line2)

Constructs a corner from the type, intersection, and lines.

```java
Corner(int type,Point intersection,LineSegment line1,LineSegment line2);
```

### transformByMatrix

Transforms the coordinates of the corner by a transformation matrix.

```java
Corner transformByMatrix(Matrix matrix);
```

**Parameters**

`matrix`: The transformation matrix.

**Return Value**

The transformed corner.
