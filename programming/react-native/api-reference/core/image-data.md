---
layout: default-layout
title: ImageData - Dynamsoft Capture Vision React Native
description: Interface ImageData of DCV React Native represents an image with its raw attributes.
keywords: image data, intermediate, capture vision, original image, result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageData

Interface `ImageData` encapsulates all of an image's data, as well as metadata. It is used to represent an image, and the image's data can then be used for further operations such as analysis, viewing, or saving.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface ImageData
```

## Properties & Methods

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`bytes`](#bytes) | *ArrayBuffer* | Represents the raw bytes of the image. |
| [`width`](#width) | *number* | Represents the width of the image in *pixels*. |
| [`height`](#height) | *number* | Represents the height of the image in *pixels*. |
| [`orientation`](#orientation) | *number* | Represents the orientation of the image as an angle. |
| [`format`](#format) | *EnumImagePixelFormat* | Represents the pixel format of the image as a [`EnumImagePixelFormat`](enum/image-pixel-format.md). |
| [`stride`](#stride) | *number* | Represents the number of bytes in a single row of the image. |

| Method | Description |
| ------ | ----------- |
| [`release`](#release) | Release the native memory. Data cannot be used after release. |

### bytes

Represents the raw bytes of the image. 

```js
buffer: ArrayBuffer;
```

### width

Represents the width of the image in *pixels*.

```js
width: number;
```

### height

Represents the height of the image in *pixels*.

```js
height: number;
```

### orientation

Represents the orientation of the image as an angle.

```js
orientation: number;
```

### format

Represents the pixel format of the image as a [`EnumImagePixelFormat`](enum/image-pixel-format.md).

```js
format: EnumPixelFormat | number;
```

### stride

Represents the number of bytes in a single row of the image.

```js
stride: number;
```

### release

Release the native memory. Data cannot be used after release.

```js
release(): void;
```