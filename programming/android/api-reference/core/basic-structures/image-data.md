---
layout: default-layout
Title: ImageData - Dynamsoft Core Module Android Edition API Reference
Description: The class ImageData of Dynamsoft Core Module represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.
Keywords: image data, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageData

The `ImageData` class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures
*Assembly:* DynamsoftCore.aar

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
| [`format`](#format) | *EnumImagePixelFormat* | The image pixel format used in the image byte array. |
| [`orientation`](#orientation) | *int* | The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file. |
| [`tag`](#tag) | *ImageTag* | The tag of the image. |

## Methods

| Method | Description |
| ------ | ----------- |
| [`toBitmap`](#tobitmap) | Transform the ImageData to an `android.graphics.Bitmap`. |
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
int format;
```

### orientation

The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file.

```java
int orientation;
```

### tag

The tag of the image.

```java
ImageTag tag;
```

### toBitmap

Transform the ImageData to a `android.graphics.Bitmap`.

```java
Bitmap toBitmap() throws CoreException;
```

**Exception**

An exception is thrown when the BPP (bit per pixel) is not supported.

**Return Value**

An `android.graphics.Bitmap` that converted from the `ImageData`.

### toString

Transform the `ImageData` to a string.

```java
String toString();
```

**Return Value**

A String that converted from the `ImageData`.
