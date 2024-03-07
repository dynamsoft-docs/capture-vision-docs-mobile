---
layout: default-layout
title: TransformedGrayscaleImageUnit - Dynamsoft Core Module Android Edition API Reference
description: The class TransformedGrayscaleImageUnit of Dynamsoft Core Module represents a unit that contains a transformed grayscale image.
keywords: transformed grayscale image, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TransformedGrayscaleImageUnit

The `TransformedGrayscaleImageUnit` class represents a unit that contains a transformed grayscale image.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class TransformedGrayscaleImageUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getImageData`](#getimagedata) | Gets the `ImageData` object as the image data of the grayscale-transformed image. |
| [`setImageData`](#setimagedata) | Sets the `ImageData` object as the image data of the grayscale-transformed image. |

### getImageData

Gets the `ImageData` object as the image data of the grayscale-transformed image.

```java
ImageData getImageData();
```

**Return Value**

The `ImageData` object as the image data of the grayscale-transformed image.

### setImageData

Sets the `ImageData` object as the image data of the grayscale-transformed image.

```java
void setImageData(ImageData imageData);
```

**Parameter**

`imageData`: The `ImageData` object as the image data of the grayscale-transformed image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
