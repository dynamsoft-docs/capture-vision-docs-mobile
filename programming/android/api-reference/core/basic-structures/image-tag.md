---
layout: default-layout
Title: ImageTag - Dynamsoft Core Module Android Edition API Reference
Description: The class ImageTag of Dynamsoft Core Module represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.
Keywords: image tag, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageTag

The `ImageTag` class represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures
*Assembly:* DynamsoftCore.aar

```java
class ImageTag
```

## Attributes

| Attributes | Description |
| ---------- | ----------- |
| [`setImageId`](#setimageid) | Set the ID of the image. |
| [`getImageId`](#getimageid) | Get the ID of the image. |
| [`getType`](#gettype) | The type of the image tag. |
| [`getDistanceMode`](#getdistancemode) | Set the capture distance mode of the image. |
| [`getDistanceMode`](#getdistancemode) | Get the capture distance mode of the image. |

### setImageId

Set the ID of the image.

```java
void setImageId(int imageId);
```

### getImageId

Get the ID of the image.

```java
int getImageId();
```

### getType

The type of the image tag.

```java
EnumImageTagType getType();
```

### setDistanceMode

Set the capture distance mode of the image.

```java
void setDistanceMode(EnumImageCaptureDistanceMode distanceMode){}
```

### getDistanceMode

Get the capture distance mode of the image.

```java
EnumImageCaptureDistanceMode getDistanceMode(){}
```
