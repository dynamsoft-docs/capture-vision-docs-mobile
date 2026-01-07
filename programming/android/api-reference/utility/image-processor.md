---
layout: default-layout
title: ImageProcessor - Dynamsoft Capture Vision Android Edition API Reference
description: The class ImageProcessor of Dynamsoft Capture Vision Android is a utility class for processing images. It provides functionality like croping or converting images.
keywords: image io, image manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageProcessor

The class `ImageProcessor` is a utility class for managing the image data. It provides functionality for saving images to files and reading images from files.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class ImageProcessor
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`cropImage`](#cropimageimagedatarect) | Crops an image based on the provided rectangle. |
| [`cropAndDeskewImage(imageData,quad,dstWidth,dstHeight,padding)`](#cropanddeskewimageimagedataquaddstwidthdstheightpaddingerrorcode) | Crops and deskew an image based on the provided quadrilateral and additional information. |
| [`cropAndDeskewImage(imageData,quad)`](#cropanddeskewimageimagedataquad) | Crops and deskew an image based on the provided quadrilateral. | 
| [`adjustBrightness`](#adjustbrightness) | Adjusts the brightness of an image. |
| [`adjustContrast`](#adjustcontrast) | Adjusts the contrast of an image. |
| [`filterImage`](#filterimage) | Applies a filter to an image. |
| [`convertToGray`](#converttograyimagedata) | Converts an image to grayscale. |
| [`convertToGray`](#converttograyimagedatargb) | Converts an image to grayscale. |
| [`convertToBinaryGlobal`](#converttobinaryglobalimagedata) | Converts an image to binary using a global threshold. |
| [`convertToBinaryGlobal`](#converttobinaryglobalimagedatathresholdinvert) | Converts an image to binary using a global threshold. |
| [`convertToBinaryLocal`](#converttobinarylocalimagedata) | Converts an image to binary using a local threshold. |
| [`convertToBinaryLocal`](#converttobinarylocalimagedatablocksizecompensationinvert) | Converts an image to binary using a local threshold. |

### cropImage(imageData,rect)

Crops an image based on the provided rectangle.

```java
ImageData cropImage(ImageData imageData, Rect rect) throws UtilityException{}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

`[in] rect`: The `Rect` to crop the image.

**Return Value**

The cropped `ImageData`.

### cropAndDeskewImage(imageData,quad,dstWidth,dstHeight,padding,errorCode)

Crops and deskews an image based on the provided quadrilateral and additional information.

```java
public ImageData cropAndDeskewImage(ImageData imageData, Quadrilateral quad, int dstWidth, int dstHeight, int padding) throws UtilityException{}
```

### cropAndDeskewImage(imageData,quad)

Crops and deskews an image based on the provided quadrilateral. The arguments dstWidth, dstHeight, and padding are set to 0.

```java
public ImageData cropAndDeskewImage(ImageData imageData, Quadrilateral quad) throws UtilityException{}
```

### adjustBrightness

Adjusts the brightness of an image.

```java
ImageData adjustBrightness(ImageData imageData, @IntRange(from = -100, to = 100) int brightness){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

`[in] brightness`: The amount to adjust the brightness by.

**Return Value**

The modified `ImageData`.

### adjustContrast

Adjusts the contrast of an image.

```java
ImageData adjustContrast(ImageData imageData, @IntRange(from = -100, to = 100) int contrast){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

`[in] contrast`: The amount to adjust the contrast by.

**Return Value**

The modified `ImageData`.

### filterImage

Applies a filter to an image.

```java
ImageData filterImage(ImageData imageData, @EnumFilterType int filterType){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

`[in] filterType`: The type of filter to apply.

**Return Value**

The modified `ImageData`.

### convertToGray(imageData)

Converts an image to grayscale.

```java
ImageData convertToGray(ImageData imageData){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

**Return Value**

The converted grayscale `ImageData`.

### convertToGray(imageData,r,g,b)

Converts an image to grayscale.

```java
ImageData convertToGray(ImageData imageData, @FloatRange(from = 0, to = 1) float r, @FloatRange(from = 0, to = 1) float g, @FloatRange(from = 0, to = 1) float b){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

`[in] r`: The weight for the red channel.

`[in] g`: The weight for the green channel.

`[in] b`: The weight for the blue channel.

**Return Value**

The converted grayscale `ImageData`.

### convertToBinaryGlobal(imageData)

Converts an image to binary using a global threshold.

```java
ImageData convertToBinaryGlobal(ImageData imageData){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

**Return Value**

The converted binary `ImageData`.

### convertToBinaryGlobal(imageData,threshold,invert)

Converts an image to binary using a global threshold.

```java
ImageData convertToBinaryGlobal(ImageData imageData, @IntRange(from = -1, to = 255) int threshold, boolean invert){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

`[in] threshold`: The threshold value.

`[in] invert`: Whether to invert the binary image.

**Return Value**

The converted binary `ImageData`.

### convertToBinaryLocal(imageData)

Converts an image to binary using a local threshold.

```java
ImageData convertToBinaryLocal(ImageData imageData){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

**Return Value**

The converted binary `ImageData`.

### convertToBinaryLocal(imageData,blockSize,compensation,invert)

Converts an image to binary using a local threshold.

```java
ImageData convertToBinaryLocal(ImageData imageData, int blockSize, int compensation, boolean invert){}
```

**Parameters**

`[in] imageData`: The `ImageData` to modify.

`[in] blockSize`: The block size for local thresholding.

`[in] compensation`: The compensation value for local thresholding.

`[in] invert`: Whether to invert the binary image.

**Return Value**

The converted binary `ImageData`.
