---
layout: default-layout
title: ImageSourceAdapter - Dynamsoft Capture Vision React Native API Reference
description: The class ImageSourceAdapter of Dynamsoft Capture Vision React Native represents an interface for fetching and buffering images.
keywords: image source adapter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceAdapter

The abstract class `ImageSourceAdapter` is an abstract class for implementing image fetching and delivering features. 

> [!Note]
> Default implementations:
> - [CameraEnhancer]({{ site.dce_react_native_api }}camera-enhancer.html): Use the camera as the image source for scanning from the video input.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
abstract class ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`addImageToBuffer`](#addimagetobuffer) | Adds an image to the internal buffer. |
| [`clearBuffer`](#clearbuffer) | Clears all images from the buffer. |
| [`destroy`](#destroy) | Destroy native instance. This object is no longer available after destroy(). |
| [`getColourChannelUsageType`](#getcolourchannelusagetype) | Get the current usage type for color channels in images. |
| [`getImageCount`](#getimagedata) | Get the current number of images in the buffer. |
| [`getImageData`](#getimagedata) | Get a buffered image. |
| [`getMaximumImageCount`](#getmaximumimagecount) | Get the maximum number of images that can be buffered. |
| [`isBufferEmpty`](#isbufferempty) | Determines whether the buffer is empty. |
| [`setColourChannelUsageType`](#setcolourchannelusagetype) | Sets the usage type for color channels in images. |
| [`setMaximumImageCount`](#setmaximumimagecount) | Sets the maximum number of images that can be buffered at any time. |
| [`startFetching`](#startfetching) | Start fetching images from the source to the Video Buffer of `ImageSourceAdapter`. |
| [`stopFetching`](#stopfetching) | Stop fetching images from the source to the Video Buffer of `ImageSourceAdapter`. |

### addImageToBuffer

Adds an image to the internal buffer.

```js
addImageToBuffer(imageData: ImageData): void
```

### clearBuffer

Clears all images from the buffer.

```js
clearBuffer(): Promise<void>
```

### destroy

Destroy native instance. This object is no longer available after destroy().

```js
destroy(): void
```

### getColourChannelUsageType

Get the current usage type for color channels in images.

```js
getColourChannelUsageType(): Promise<EnumColourChannelUsageType>
```

### getImageCount

Get the current number of images in the buffer.

```js
getImageCount(): Promise<number>
```

### getImageData

Get a buffered image.

```js
getImageData(): undefined | null | ImageData
```

### getMaximumImageCount

Get the maximum number of images that can be buffered.

```js
getMaximumImageCount(): Promise<number>
```

### isBufferEmpty

Determines whether the buffer is empty.

```js
isBufferEmpty(): Promise<boolean>
```

### setColourChannelUsageType

Sets the usage type for color channels in images.

```js
setColourChannelUsageType(type: EnumColourChannelUsageType): Promise<void>
```

### setMaximumImageCount

Sets the maximum number of images that can be buffered at any time.

```js
setMaximumImageCount(count: number): Promise<void>
```

### startFetching

Start fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

```js
startFetching(): void
```

### stopFetching

Stop fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

```js
stopFetching(): void
```

