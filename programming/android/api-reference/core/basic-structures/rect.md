---
layout: default-layout
title: DSRect - Dynamsoft Core Module Android Edition API Reference
description: The class DSRect of Dynamsoft Core Module Android edition represents a rectangle in 2D space, which contains four integer values that specify the top, left, right, and bottom edges of the rectangle.
keywords: rectangle, 2D space, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSRect

The `DSRect` class represents a rectangle in 2D space, which contains four integer values that specify the top, left, right, and bottom edges of the rectangle.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
class DSRect
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`top`](#top) | *float* | The distance between the top of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`left`](#left) | *float* | The distance between the left of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`right`](#right) | *float* | The distance between the right of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`bottom`](#bottom) | *float* | The distance between the bottom of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`measuredInPercentage`](#measuredinpercentage) | *boolean* | Indicates if the rectangle's measurements are in percentages. |

### top

The distance between the top of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

```java
float top;
```

### left

The distance between the left of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

```java
float left;
```

### right

The distance between the right of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

```java
float right;
```

### bottom

The distance between the bottom of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length.

```java
float bottom;
```

### measuredInPercentage

Sets whether to use percentages to measure the region size.

```java
boolean isMeasuredInPercentage;
```
