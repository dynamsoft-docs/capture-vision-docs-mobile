---
layout: default-layout
Title: RawImageResultItem - Dynamsoft Core Module Android Edition API Reference
Description: The class RawImageResultItem of Dynamsoft Core Module represents a captured raw image result item, which provides an property to get the image data.
Keywords: raw image result item, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RawImageResultItem

The `RawImageResultItem` class represents a captured raw image result item, which is a derived class of `CapturedResultItem` and provides a property to get the image data.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures
*Assembly:* DynamsoftCore.aar

```java
class RawImageResultItem extends CapturedResultItem
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`getImageData`](#getimagedata) | *ImageData* | Get the image data of the captured raw image result item. |

### getImageData

Get the image data of the captured raw image result item.

```java
ImageData getImageData();
```

**Return Value**

The image data of the captured raw image result item.
