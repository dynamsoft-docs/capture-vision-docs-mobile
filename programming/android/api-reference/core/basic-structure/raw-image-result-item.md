---
layout: default-layout
Title: DSRawImageResultItem - Dynamsoft Core Module Android Edition API Reference
Description: The class DSRawImageResultItem of Dynamsoft Core Module represents a captured raw image result item, which provides an property to get the image data.
Keywords: raw image result item, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSRawImageResultItem

The `DSRawImageResultItem` class represents a captured raw image result item, which is a derived class of `CapturedResultItem` and provides a property to get the image data.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class RawImageResultItem extends CapturedResultItem
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageData`](#imagedata) | *DSImageData \** | The image data of the captured raw image result item. |

### imageData

The image data of the captured raw image result item.

```java
var imageData: ImageData { get }
```
