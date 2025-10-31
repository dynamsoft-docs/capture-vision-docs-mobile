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
| [`ImageTag`](#imagetag-1) | The constructor. |
| [`setImageId`](#setimageid) | Set the ID of the image. The ID is the unique identifier of the image. |
| [`getImageId`](#getimageid) | Get the ID of the image. The ID is the unique identifier of the image. |
| [`getTagType`](#gettagtype) | The type of the image tag. |
| [`setDistanceMode`](#setdistancemode) | Set the capture distance mode of the image. |
| [`getDistanceMode`](#getdistancemode) | Get the capture distance mode of the image. |

### ImageTag

The constructor.

```java
ImageTag();
```

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

### getTagType

The type of the image tag.

```java
int getTagType();
```

**Return Value**

The type of the image tag. Refer to [`EnumImageTagType`]({{ site.dcv_android_api }}core/enum/image-tag-type.html).

### setDistanceMode

Set the capture distance mode of the image.

```java
void setDistanceMode(int distanceMode)
```

**Parameters**

`[in] distanceMode`: The capture distance mode of the image. Refer to [`EnumImageCaptureDistanceMode`]({{ site.dcv_android_api }}core/enum/image-capture-distance-mode.html).

### getDistanceMode

Get the capture distance mode of the image.

```java
int getDistanceMode()
```

**Return Value**

The distance mode of the image. Refer to [`EnumImageCaptureDistanceMode`]({{ site.dcv_android_api }}core/enum/image-capture-distance-mode.html).
