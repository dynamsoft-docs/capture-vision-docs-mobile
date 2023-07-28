---
layout: default-layout
Title: TextureDetectionResultUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class TextureDetectionResultUnit of Dynamsoft Core Module represents an intermediate result unit for texture detection, which contains the x-direction spacing and y-direction spacing of the texture stripes.
Keywords: texture detection, Java, Kotlin
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
