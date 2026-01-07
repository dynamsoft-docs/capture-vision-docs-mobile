---
layout: default-layout
title: ImageProcessor - Dynamsoft Capture Vision MAUI API Reference
description: The class ImageProcessor of Dynamsoft Capture Vision MAUI is a utility class that provides functionality for processing.
keywords: image processor, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageProcessor

The `ImageProcessor` class is a utility class that provides functionality for processing.

## Definition

*Namespace:* Dynamsoft.Utility.Maui

*Assembly:* Dynamsoft.Utility.Maui

```csharp
class ImageProcessor
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`CropImage`](#cropimagerect) | Crops an image based on the provided rectangle or quadrilateral. |
| [`CropAndDeskewImage(imageData,quadrilateral,dstWidth,dstHeight,padding)`](#cropanddeskewimageimagedataquadrilateraldstwidthdstheightpaddingerrorcode) | Crops and deskew an image based on the provided quadrilateral and additional information. |
| [`CropAndDeskewImage(imageData,quadrilateral)`](#cropanddeskewimageimagedataquadrilateral) | Crops and deskew an image based on the provided quadrilateral. |
| [`AdjustBrightness`](#adjustbrightness) | Adjusts the brightness of an image. |
| [`AdjustContrast`](#adjustcontrast) | Adjusts the contrast of an image. |
| [`FilterImage`](#filterimage) | Applies a filter to an image. |
| [`ConvertToGray`](#converttogray) | Converts an image to grayscale. |
| [`ConvertToGray`](#converttograyrgb) | Converts an image to grayscale with the specified RGB value. |
| [`ConvertToBinaryGlobal`](#converttobinaryglobal) | Converts an image to binary using threshold binarization mode. |
| [`ConvertToBinaryGlobal`](#converttobinaryglobalthresholdinvert) | Converts an image to binary using threshold binarization mode with the specified threshold. |
| [`ConvertToBinaryLocal`](#converttobinarylocal) | Converts an image to binary using local-block binarization mode. |
| [`ConvertToBinaryLocal`](#converttobinarylocalblocksizecompensationinvert) | Converts an image to binary using local-block binarization mode with the specified block size and compensation. |

### CropImage(rect)

Crops an image based on the provided rectangle.

```csharp
ImageData? CropImage(ImageData imageData, DMRect rect);
```

**Parameters**

`[in] imageData`: The `ImageData` to crop.

`[in] rect`: The `DMRect` specifying the region to crop.

**Return Value**

The cropped `ImageData`.

### CropAndDeskewImage(imageData,quadrilateral,dstWidth,dstHeight,padding,errorCode)

Crops and deskews an image based on the provided quadrilateral and additional information.

```csharp
partial ImageData? CropAndDeskewImage(ImageData imageData, Quadrilateral quadrilateral, int dstWidth, int dstHeight, int padding);
```

**Parameters**

`[in] imageData`: The `ImageData` to crop.

`[in] quadrilateral`: The `Quadrilateral` specifying the region to crop.

`[in] dstWidth`: The width of the destination image.

`[in] dstHeight`: The height of the destination image.

`[in] padding`: The padding value to be added to the destination image.

### CropAndDeskewImage(imageData,quadrilateral)

Crops and deskews an image based on the provided quadrilateral. The arguments dstWidth, dstHeight, and padding are set to 0.

```csharp
partial ImageData? CropAndDeskewImage(ImageData imageData, Quadrilateral quadrilateral);
```

**Parameters**

`[in] imageData`: The `ImageData` to crop.

`[in] quadrilateral`: The `Quadrilateral` specifying the region to crop.

### AdjustBrightness

Adjusts the brightness of an image.

```csharp
ImageData? AdjustBrightness(ImageData imageData, int brightness);
```

**Parameters**

`[in] imageData`: The `ImageData` to adjust.

`[in] brightness`: The amount to adjust the brightness by.

**Return Value**

The brightness-adjusted `ImageData`.

### AdjustContrast

Adjusts the contrast of an image.

```csharp
ImageData? AdjustContrast(ImageData imageData, int contrast);
```

**Parameters**

`[in] imageData`: The `ImageData` to adjust.

`[in] contrast`: The amount to adjust the contrast by.

**Return Value**

The contrast-adjusted `ImageData`.

### FilterImage

Applies a filter to an image.

```csharp
ImageData? FilterImage(ImageData imageData, EnumFilterType type);
```

**Parameters**

`[in] imageData`: The `ImageData` to filter.

`[in] type`: The `EnumFilterType` specifying the filter type.

**Return Value**

The filtered `ImageData`.

### ConvertToGray

Converts a colour image to a grayscale image.

```csharp
ImageData? ConvertToGray(ImageData imageData);
```

**Parameters**

`[in] imageData`: The `ImageData` to convert.

**Return Value**

The grayscale `ImageData`.

### ConvertToGray(rgb)

Converts a colour image to a grayscale image with the specified RGB value.

```csharp
ImageData? ConvertToGray(ImageData imageData, float r, float g, float b);
```

**Parameters**

`[in] imageData`: The `ImageData` to convert.

`[in] r`: The red component weight.

`[in] g`: The green component weight.

`[in] b`: The blue component weight.

**Return Value**

The grayscale `ImageData`.

### ConvertToBinaryGlobal

Converts an image to binary using threshold binarization mode.

```csharp
ImageData? ConvertToBinaryGlobal(ImageData imageData);
```

**Parameters**

`[in] imageData`: The `ImageData` to convert.

**Return Value**

The binary `ImageData`.

### ConvertToBinaryGlobal(threshold,invert)

Converts an image to binary using threshold binarization mode with the specified threshold.

```csharp
ImageData? ConvertToBinaryGlobal(ImageData imageData, int threshold, bool invert);
```

**Parameters**

`[in] imageData`: The `ImageData` to convert.

`[in] threshold`: The threshold value.

`[in] invert`: A flag indicating whether to invert the binary image.

**Return Value**

The binary `ImageData`.

### ConvertToBinaryLocal

Converts an image to binary using local-block binarization mode.

```csharp
ImageData? ConvertToBinaryLocal(ImageData imageData);
```

**Parameters**

`[in] imageData`: The `ImageData` to convert.

**Return Value**

The binary `ImageData`.

### ConvertToBinaryLocal(blockSize,compensation,invert)

Converts an image to binary using local-block binarization mode with the specified block size and compensation.

```csharp
ImageData? ConvertToBinaryLocal(ImageData imageData, int blockSize, int compensation, bool invert);
```

**Parameters**

`[in] imageData`: The `ImageData` to convert.

`[in] blockSize`: The size of the block.

`[in] compensation`: The compensation value.

`[in] invert`: A flag indicating whether to invert the binary image.

**Return Value**

The binary `ImageData`.
