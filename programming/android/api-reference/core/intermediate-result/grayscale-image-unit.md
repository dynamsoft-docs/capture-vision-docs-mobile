---
layout: default-layout
Title: DSGrayscaleImageUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class DSGrayscaleImageUnit of Dynamsoft Core Module represents a unit that contains a grayscale image. It is derived from the DSIntermediateResultUnit class.
Keywords: grayscale image unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSGrayscaleImageUnit

The `DSGrayscaleImageUnit` class represents a unit that contains a grayscale image. It is derived from the `DSIntermediateResultUnit` class.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class GrayscaleImageUnit: IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | A `DSImageData` object as the image data of the grayscale image. |

### imageData

A `DSImageData` object as the image data of the grayscale image.

```java
var imageData: ImageData? { get set }
```
