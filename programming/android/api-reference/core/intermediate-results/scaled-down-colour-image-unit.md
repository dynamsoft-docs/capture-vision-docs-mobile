---
layout: default-layout
title: ScaledDownColourImageUnit - Dynamsoft Core Module Android Edition API Reference
description: The class ScaledDownColourImageUnit of Dynamsoft Core Module represents a unit that contains a down-scaled colour image.
keywords: scaled down colour image unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ScaledDownColourImageUnit

The `ScaledDownColourImageUnit` class represents a unit that contains a down-scaled colour image.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class ScaledDownColourImageUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getImageData`](#getimagedata) | Gets the `ImageData` object as the image data of the down-scaled colour image. |
| [`setImageData`](#setimagedata) | Sets the `ImageData` object as the image data of the down-scaled colour image. |

### getImageData

Gets the `ImageData` object as the image data of the down-scaled colour image.

```java
ImageData getImageData();
```

**Return Value**

The `ImageData` object as the image data of the down-scaled colour image.

### setImageData

Sets the `ImageData` object as the image data of the down-scaled colour image.

```java
int setImageData(ImageData imageData);
```

**Parameters**

`imageData`: The `ImageData` object as the image data of the down-scaled colour image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
