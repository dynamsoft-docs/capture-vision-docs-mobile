---
layout: default-layout
title: TextRemovedBinaryImageUnit - Dynamsoft Core Module Android Edition API Reference
description: The class TextRemovedBinaryImageUnit of Dynamsoft Core Module represents a unit that contains a text-removed binary image.
keywords: text-removed binary image, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextRemovedBinaryImageUnit

The `TextRemovedBinaryImageUnit` class represents a unit that contains a text-removed binary image.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class TextRemovedBinaryImageUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getImageData`](#getimagedata) | Gets the `ImageData` object as the image data of the text-removed binary image. |
| [`setImageData`](#setimagedata) | Sets the `ImageData` object as the image data of the text-removed binary image. |

### getImageData

Gets the `ImageData` object as the image data of the text-removed binary image.

```java
ImageData getImageData();
```

**Return Value**

The `ImageData` object as the image data of the text-removed binary  image.

### setImageData

Sets the `ImageData` object as the image data of the text-removed binary image.

```java
int setImageData(ImageData imageData);
```

**Parameter**

`imageData`: The `ImageData` object as the image data of the text-removed binary image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
