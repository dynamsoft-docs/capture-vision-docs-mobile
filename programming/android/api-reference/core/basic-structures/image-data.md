---
layout: default-layout
title: ImageData - Dynamsoft Core Module Android Edition API Reference
description: The class ImageData of Dynamsoft Core Module represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.
keywords: image data, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageData

The `ImageData` class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class ImageData
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`bytes`](#bytes) | *byte[]* | The image data content in a byte array. |
| [`width`](#width) | *int* | The width of the image in pixels. |
| [`height`](#height) | *int* | The height of the image in pixels. |
| [`stride`](#stride) | *int* | The stride (or scan width) of the image. |
| [`format`](#format) | *int* | The image pixel format used in the image byte array. |
| [`orientation`](#orientation) | *int* | The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file. |
| [`tag`](#tag) | *[ImageTag](image-tag.md)* | The tag of the image. |

## Methods

| Method | Description |
| ------ | ----------- |
| [`ImageData`](#imagedata-1) | The constructor. |
| [`toBitmap`](#tobitmap) | Transform the ImageData to an `android.graphics.Bitmap`. |
| [`fromBitmap`](#frombitmap) | Convert an `android.graphics.Bitmap` to an ImageData. |
| [`toString`](#tostring) | Transform the ImageData to a string. |

### bytes

The image data content in a byte array.

```java
byte[] bytes;
```

### width

The width of the image in pixels.  

```java
int width;
```

### height

The height of the image in pixels.  

```java
int height;
```

### stride

The stride (or scan width) of the image.

```java
int stride;
```

### format

The image pixel format used in the image byte array.

```java
@EnumImagePixelFormat
int format;
```

Related APIs:

- [EnumImagePixelFormat]({{ site.dcv_android_api }}core/enum/image-pixel-format.html?lang=android)

### orientation

The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file.

```java
int orientation;
```

### tag

The tag of the image.

```java
ImageTag imageTag;
```

### ImageData

The constructor.

```java
ImageData();
```

### toBitmap

Transform the ImageData to a `android.graphics.Bitmap`.

```java
Bitmap toBitmap() throws CoreException;
```

**Exception**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_BPP_NOT_SUPPORTED | -10007 | The pixel format is not supported or the ImageData is invalid. |

**Return Value**

An `android.graphics.Bitmap` that converted from the `ImageData`.

### fromBitmap

Convert an `android.graphics.Bitmap` to an ImageData.

```java
static ImageData fromBitmap(Bitmap bitmap);
```

### toString

Transform the `ImageData` to a string.

```java
String toString();
```

**Return Value**

A String that converted from the `ImageData`.
