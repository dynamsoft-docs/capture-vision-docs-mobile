---
layout: default-layout
Title: DSImageTag - Dynamsoft Core Module Android Edition API Reference
Description: The class DSImageTag of Dynamsoft Core Module represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.
Keywords: image tag, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageTag

The `DSImageTag` class represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class ImageTag
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`imageId`](#imageid) | *NSInteger* | The ID of the image. |
| [`type`](#type) | *DSImageTagType* | The type of the image tag. |
| [`distanceMode`](#distancemode) | *DSImageCaptureDistanceMode* | The capture distance mode of the image. |

### imageId

The ID of the image.

```java
var imageId: Int { get }
```

### type

The type of the image tag.

```java
var type: EnumImageTagType { get }
```

### distanceMode

The capture distance mode of the image.

```java
var distanceMode: EnumImageCaptureDistanceMode { get set }
```
