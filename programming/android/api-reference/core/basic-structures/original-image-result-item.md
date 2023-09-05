---
layout: default-layout
title: OriginalImageResultItem - Dynamsoft Core Module Android Edition API Reference
description: The class OriginalImageResultItem of Dynamsoft Core Module represents a captured original image result item, which provides an property to get the image data.
keywords: original image result item, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# OriginalImageResultItem

The `OriginalImageResultItem` class represents a captured original image result item, which is a derived class of `CapturedResultItem` and provides a property to get the image data.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
class OriginalImageResultItem extends CapturedResultItem
```

## Attributes

| Methods | Description |
| ------- | ----------- |
| [`getImageData`](#getimagedata) | Get the image data of the captured original image result item. |

### getImageData

Get the image data of the captured original image result item.

```java
ImageData getImageData();
```

**Return Value**

The image data of the captured original image result item.
