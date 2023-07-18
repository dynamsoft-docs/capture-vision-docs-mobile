---
layout: default-layout
Title: DSTextureDetectionResultUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class DSTextureDetectionResultUnit of Dynamsoft Core Module represents an intermediate result unit for texture detection, which contains the x-direction spacing and y-direction spacing of the texture stripes.
Keywords: texture detection, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextureDetectionResultUnit

The `DSTextureDetectionResultUnit` class represents an intermediate result unit for texture detection, which contains the x-direction spacing and y-direction spacing of the texture stripes.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class TextureDetectionResultUnit extends IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`xSpacing`](#xspacing) | *NSInteger* | X-direction spacing of the texture stripes. |
| [`ySpacing`](#yspacing) | *NSInteger* | Y-direction spacing of the texture stripes. |

### xSpacing

X-direction spacing of the texture stripes.

```java
var xSpacing: Int { get set }
```

### ySpacing

Y-direction spacing of the texture stripes.

```java
var ySpacing: Int { get set }
```
