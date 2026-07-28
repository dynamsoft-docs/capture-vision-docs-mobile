---
layout: default-layout
title: LayoutElement - Dynamsoft Capture Vision Android Edition API Reference
description: The class LayoutElement of Dynamsoft Capture Vision Android edition represents an element in a layout analysis.
keywords: layout element, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutElement

The `LayoutElement` class represents an element in a layout analysis.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class LayoutElement
```

## Attributes

| Attribute | Type | Description |
| --------- | ---- | ----------- |
| [`quad`](#quad) | *Quadrilateral* | Geometric coordinates of the element. |
| [`source`](#source) | *int* | Origin of the element. |

### quad

Geometric coordinates of the element.

```java
Quadrilateral quad;
```

### source

Origin of the element.

```java
@EnumLayoutElementSource
int source;
```
