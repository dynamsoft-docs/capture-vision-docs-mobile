---
layout: default-layout
title: BinaryImageUnit - Dynamsoft Core Module Android Edition API Reference
description: The class BinaryImageUnit of Dynamsoft Core Module represents a unit that contains a binary image.
keywords: binary image, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BinaryImageUnit

The `BinaryImageUnit` class represents a unit that contains a binary image.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class BinaryImageUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getImageData`](#getimagedata) | Gets the `ImageData` object as the image data of the binary image. |
| [`setImageData`](#setimagedata) | Sets the `ImageData` object as the image data of the binary image. |

### getImageData

Gets the `ImageData` object as the image data of the binary image.

```java
ImageData getImageData();
```

**Return Value**

The `ImageData` object as the image data of the binary image.

### setImageData

Sets the `ImageData` object as the image data of the binary image.

```java
int setImageData(ImageData imageData);
```

**Parameters**

`imageData`: The `ImageData` object as the image data of the binary image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
