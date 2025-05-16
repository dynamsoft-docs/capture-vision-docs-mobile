---
layout: default-layout
title: ImageTag - Dynamsoft Core Module Android Edition API Reference
description: The class ImageTag of Dynamsoft Core Module represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.
keywords: image tag, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageTag

The `ImageTag` class represents an image tag that can be attached to an image in a system. It contains information about the image, such as the image ID and the image capture distance mode.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class ImageTag
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`setImageId`](#setimageid) | Set the ID of the image. The ID is the unique identifier of the image. |
| [`getImageId`](#getimageid) | Get the ID of the image. The ID is the unique identifier of the image. |
| [`getType`](#gettype) | The type of the image tag. |
| [`setDistanceMode`](#setdistancemode) | Set the capture distance mode of the image. |
| [`getDistanceMode`](#getdistancemode) | Get the capture distance mode of the image. |

### setImageId

Set the ID of the image. The ID is the unique identifier of the image.

```java
void setImageId(int imageId);
```

**Parameters**

`[in] imageId`: The id of image for identification.

### getImageId

Get the ID of the image. The ID is the unique identifier of the image.

```java
int getImageId();
```

**Return Value**

The ID of the image.

### getType

The type of the image tag.

```java
EnumImageTagType getType();
```

**Return Value**

The [`EnumImageTagType`]({{ site.dcv_android_api }}core/enum/image-tag-type.html) of the image.

### setDistanceMode

Set the capture distance mode of the image.

```java
void setDistanceMode(EnumImageCaptureDistanceMode distanceMode)
```

**Parameters**

`[in] distanceMode`: The capture distance mode of the image.

### getDistanceMode

Get the capture distance mode of the image.

```java
EnumImageCaptureDistanceMode getDistanceMode()
```

**Return Value**

The [`EnumImageCaptureDistanceMode`]({{ site.dcv_android_api }}core/enum/image-capture-distance-mode.html) of the image.
