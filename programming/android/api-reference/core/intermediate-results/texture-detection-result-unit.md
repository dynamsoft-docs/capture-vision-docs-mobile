---
layout: default-layout
title: TextureDetectionResultUnit - Dynamsoft Core Module Android Edition API Reference
description: The class TextureDetectionResultUnit of Dynamsoft Core Module represents an intermediate result unit for texture detection, which contains the x-direction spacing and y-direction spacing of the texture stripes.
keywords: texture detection, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextureDetectionResultUnit

The `TextureDetectionResultUnit` class represents an intermediate result unit for texture detection, which contains the x-direction spacing and y-direction spacing of the texture stripes.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class TextureDetectionResultUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getXSpacing`](#getxspacing) | Gets the X-direction spacing of the texture stripes. |
| [`getYSpacing`](#getyspacing) | Gets the Y-direction spacing of the texture stripes. |
| [`setXSpacing`](#setxspacing) | Sets the X-direction spacing of the texture stripes. |
| [`setYSpacing`](#setyspacing) | Sets the Y-direction spacing of the texture stripes. |

### getXSpacing

Gets the X-direction spacing of the texture stripes.

```java
int getXSpacing()
```

**Return Value**

The X-direction spacing of the texture stripes.

### getYSpacing

Gets the Y-direction spacing of the texture stripes.

```java
int getYSpacing()
```

**Return Value**

The Y-direction spacing of the texture stripes.

### setXSpacing

Sets the X-direction spacing of the texture stripes.

```java
void setXSpacing(int xSpacing)
```

**Parameter**

`[in] xSpacing`: The X-direction spacing of the texture stripes.

### setYSpacing

Sets the Y-direction spacing of the texture stripes.

```java
void setYSpacing(int ySpacing)
```

**Parameter**

`[in] ySpacing`: The Y-direction spacing of the texture stripes.
