---
layout: default-layout
title: ImageData - Dynamsoft Capture Vision MAUI API Reference
description: The class ImageData of DCV MAUI represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.
keywords: image data
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageData

The `ImageData` class represents image data, which contains the image bytes, width, height, stride, pixel format, orientation and a tag.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
class ImageData
```

## Methods & Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`Bytes`](#bytes) | *byte[]* | The image data content in a byte array. |
| [`Width`](#width) | *int* | The width of the image in pixels. |
| [`Height`](#height) | *int* | The height of the image in pixels. |
| [`Stride`](#stride) | *int* | The stride (or scan width) of the image. |
| [`Format`](#format) | *[EnumImagePixelFormat]({{ site.dcv_maui_api }}core/enum/image-pixel-format.html)* | The image pixel format used in the image byte array. |
| [`Orientation`](#orientation) | *int* | The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file. |

| Method | Description |
| ------ | ----------- |
| [`ImageData`](#imagedata-1) | The constructor. |

### Bytes

The image data content in a byte array.

```csharp
byte[] Bytes { get; set; }
```

### Width

The width of the image in pixels.

```csharp
int Width { get; set; }
```

### Height

The height of the image in pixels.

```csharp
int Height { get; set; }
```

### Stride

The stride (or scan width) of the image.

```csharp
int Stride { get; set; }
```

### Format

The image pixel format used in the image byte array, defined in the [`EnumImagePixelFormat`]({{ site.dcv_maui_api }}core/enum/image-pixel-format.html).

```csharp
EnumImagePixelFormat Format { get; set; }
```

### Orientation

The orientation information of the image. The library is able to read the orientation information from the EXIF data of the image file.

```csharp
int Orientation { get; set; }
```

### ImageData

The constructor.

```csharp
ImageData(byte[] bytes, int width, int height, int stride, EnumImagePixelFormat format, int orientation);
```
