---
layout: default-layout
title: ImageDrawer Class - Dynamsoft Capture Vision React Native
description: ImageDrawer class of DCV React Native provides API to render shapes on images.
keywords: image drawer, intermediate, capture vision, original image, result, draw
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageDrawer

The `ImageDrawer` class provides API to render geometric shapes such as quadrilaterals on images. This class comes in handy when you want to add annotations to an image obtained from a `CapturedResult` or from the `IntermediateResultManager`.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
class ImageDrawer
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`drawOnImage`](#drawonimage) | Draws quadrilaterals on the image with the specified style parameters. |

### drawOnImage

Draws quadrilaterals on the image with the specified style parameters.

```js
drawOnImage(imageData: ImageData | null | undefined, quads: Quadrilateral[] | null | undefined, colour: number | ColorValue, thickness: number): ImageData | null | undefined
```

**Parameters**

`imageData`: The source image to draw on.

`quads`: List of Quadrilateral objects to render onto the image.

`colour`: ARGB colour value (0xAARRGGBB format)

`thickness`: The line thickness in pixels.

**Returns**

An [`ImageData`](../core/image-data.md) object that represents the new image with the rendered shapes.
