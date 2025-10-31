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

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class DSRect
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`top`](#top) | *float* | The distance between the top of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`left`](#left) | *float* | The distance between the left of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`right`](#right) | *float* | The distance between the right of the rect and the y-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the width of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`bottom`](#bottom) | *float* | The distance between the bottom of the rect and the x-axis. If measuredInPercentage = 1, the value specifies the percentage comparing with the height of the parent. If measuredInPercentage = 0, the value specifies a pixel length. |
| [`measuredInPercentage`](#measuredinpercentage) | *boolean* | Indicates if the rectangle's measurements are in percentages. |

| Method | Description |
| ------ | ----------- |
| [`DSRect`](#dsrect-1) | The constructor. |
| [`DSRect(left,top,right,bottom,measuredInPercentage)`](#dsrectlefttoprightbottommeasuredinpercentage) | Constructs a DSRect from the specified parameters. |
| [`fromJson`](#fromjson) | Constructs a DSRect from a JSON string. |

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

### DSRect

The constructor.

```java
DSRect();
```

### DSRect(left,top,right,bottom,measuredInPercentage)

Constructs a DSRect from the specified parameters.

```java
DSRect(float left, float top, float right, float bottom, boolean measuredInPercentage);
```

### fromJson

Constructs a DSRect from a JSON string.

```java
DSRect fromJson(String jsonString);
```
