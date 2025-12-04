---
layout: default-layout
title: ImageIO Class - Dynamsoft Capture Vision React Native
description: ImageIO class of DCV React Native provides API to read and write image data to the file system.
keywords: image io, intermediate, capture vision, original image, result, file system, save
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageIO

The `ImageIO` class provides API to handle image input/output operations such as saving images to the file system. This class allows the library to read and write image data to the file system. 

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
class ImageIO
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`readFromFile`](#readfromfile) | Reads an image from a file at the specified file path and returns an [`ImageData`](../core/image-data.md) object that represents the image. |
| [`readFromMemory`](#readfrommemory) | Reads an image from ArrayBuffer memory. |
| [`saveToFile`](#savetofile) | Saves the provided [`ImageData`](../core/image-data.md) object (which represents an image) to a file at the specified file path. |
| [`saveToMemory`](#savetomemory) | Saves the provided [`ImageData`](../core/image-data.md) object (which represents an image) to ArrayBuffer memory. |

### readFromFile

Reads an image from a file at the specified file path and returns an [`ImageData`](../core/image-data.md) object that represents the image.

```js
readFromFile(path: string | null | undefined): ImageData | null | undefined
```

**Parameters**

`path`: The absolute file path, name and extension name, as a string, of the image to be read.

**Returns**

The image data, of type [`ImageData`](../core/image-data.md), or null if the image cannot be read.

### readFromMemory

Reads an image from ArrayBuffer memory.

```js
readFromMemory(data: ArrayBuffer | null | undefined): ImageData | null | undefined
```

**Parameters**

`data`: The image data, of type ArrayBuffer.

**Returns**

The image data, of type [`ImageData`](../core/image-data.md), or null if the image cannot be read.

### saveToFile

Saves the provided [`ImageData`](../core/image-data.md) object (which represents an image) to a file at the specified file path.

```js
saveToFile(imageData: ImageData | null | undefined, path: string | null | undefined, overWrite: boolean): void
```

**Parameters**

`imageData`: The image data, of type [`ImageData`](../core/image-data.md).

`path`: The absolute file path, name and extension name, as a string, of the image to be saved.

`overWrite`: Whether to overwrite the file if it already exists.

### saveToMemory

Saves an image to the specified path and format. The desired file format is inferred from the file extension provided in the path parameter.

```js
saveToMemory(imageData: ImageData | null | undefined, format: EnumImageFileFormat): ArrayBuffer | null | undefined
```

`imageData`: The image to be saved, of type [`ImageData`](../core/image-data.md).
`format`: The format of the image data, of type [`EnumImageFileFormat`](../core/enum/image-file-format.md).
