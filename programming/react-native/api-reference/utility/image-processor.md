---
layout: default-layout
title: ImageProcessor Class - Dynamsoft Capture Vision React Native
description: ImageProcessor class of DCV React Native provides API to crop images based on specified regions.
keywords: image processor, intermediate, capture vision, original image, crop
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageProcessor

The `ImageProcessor` class provides API to crop images based on specified regions.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
class ImageProcessor
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`cropImage`](#cropimage) | Crops the image (as an [`ImageData`](../core/image-data.md) object) to the region defined by the rectangle. |
| [`cropAndDeskewImage`](#cropanddeskewimage) | Crops the image (as an [`ImageData`](../core/image-data.md) object) to the region defined by the Quadrilateral. |
| [`adjustBrightness`](#adjustbrightness) | Adjusts the brightness of the image (as an [`ImageData`](../core/image-data.md) object) based on the specified brightness value. |
| [`adjustContrast`](#adjustcontrast) | Adjusts the contrast of the image (as an [`ImageData`](../core/image-data.md) object) based on the specified contrast value. |
| [`filterImage`](#filterimage) | Applies a filter (represented with [`EnumFilterType`](enum/filter-type.md)) to the image (as an [`ImageData`](../core/image-data.md) object). |
| [`convertToGray`](#converttogray) | Converts the image (as an [`ImageData`](../core/image-data.md) object) to grayscale using specified channel weights. |
| [`convertToBinaryGlobal`](#converttobinaryglobal) | Converts the image (as an [`ImageData`](../core/image-data.md) object) to a binary (black and white) format using global thresholding. |
| [`convertToBinaryLocal`](#converttobinarylocal) | Converts the image (as an [`ImageData`](../core/image-data.md) object) to a binary (black and white) format using local adaptive thresholding. |

### cropImage

Crops the image (as an [`ImageData`](../core/image-data.md) object) to the region defined by the rectangle.

```js
cropImage(imageData: ImageData | null | undefined, rect: DSRect | null | undefined): ImageData | null | undefined
```

**Remarks**

The method returns an [`ImageData`](../core/image-data.md) object that represents the newly cropped image. The method returns `null` if the cropping fails (invalid rectangle, out of bounds, a null `ImageData` object, etc.).

### cropAndDeskewImage

Crops the image (as an [`ImageData`](../core/image-data.md) object) to the region defined by the Quadrilateral.

```js
cropAndDeskewImage(imageData: ImageData | null | undefined, quad: Quadrilateral | null | undefined, dstWidth: number = 0, dstHeight: number = 0, padding: number = 0): ImageData | undefined | null
```

**Remarks**

The `quadrilateral` input parameter defines the region to extract as four corner points. The method returns an [`ImageData`](../core/image-data.md) object that represents the newly cropped image. The method returns `null` if the cropping fails (invalid Quadrilateral, out of bounds, a null `ImageData` object, etc.).

### adjustBrightness

Adjusts the brightness of the image (as an [`ImageData`](../core/image-data.md) object) based on the specified brightness value.

```js
adjustBrightness(imageData: ImageData | null | undefined, brightness: number): ImageData | null | undefined
```

**Remarks**

The `brightness` input parameter ranges from -100 to 100. Positive values increase brightness while negative values decrease it. The method returns `null` if the adjustment fails.

### adjustContrast

Adjusts the contrast of the image (as an [`ImageData`](../core/image-data.md) object) based on the specified contrast value.

```js
adjustContrast(imageData: ImageData | null | undefined, contrast: number): ImageData | null | undefined
```

**Remarks**

The `contrast` input parameter ranges from -100 to 100. Positive values increase brightness while negative values decrease it. The method returns `null` if the adjustment fails.

### filterImage

Applies a filter (represented with [`EnumFilterType`](enum/filter-type.md)) to the image (as an [`ImageData`](../core/image-data.md) object).

```js
filterImage(imageData: ImageData | null | undefined, filterType: EnumFilterType): ImageData | null | undefined
```

**Remarks**

The method returns `null` if the filtering fails.

### convertToGray

Converts the image (as an [`ImageData`](../core/image-data.md) object) to grayscale using specified channel weights.

```js
convertToGray(imageData: ImageData | null | undefined, r: number = 0.3, g: number = 0.59, b: number = 0.11): ImageData | null | undefined
```

**Remarks**

- `r`: Weight of the red channel (default value is 0.3).
- `g`: Weight of the green channel (default value is 0.59).
- `b`: Weight of the blue channel (default value is 0.11).

The method returns `null` if the conversion fails.

### convertToBinaryGlobal

Converts the image (as an [`ImageData`](../core/image-data.md) object) to a binary (black and white) format using global thresholding.

```js
convertToBinaryGlobal(imageData: ImageData | null | undefined, threshold: number = -1, invert: boolean = false)
```

Remarks

- `threshold`: A value that ranges between 0 and 255. If -1, Otsu's method is used to determine the optimal threshold.
- `inverse`: If `true`, inverts the binary colours, resulting in a negative filter on the image.

### convertToBinaryLocal

Converts the image (as an [`ImageData`](../core/image-data.md) object) to a binary (black and white) format using local adaptive thresholding.

```js
convertToBinaryLocal(imageData: ImageData | null | undefined, blockSize: number = 0, compensation: number = 0, invert: boolean = false)
```

**Remarks**

- `blockSize`: Size of the local region (must be odd and >= 3).
- `compensation`: Value to adjust the threshold (typically 0-10).
- `inverse`: If `true`, inverts the binary colours, resulting in a negative filter on the image.
