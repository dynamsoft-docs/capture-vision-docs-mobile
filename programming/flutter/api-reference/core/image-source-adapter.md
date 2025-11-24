---
layout: default-layout
title: ImageSourceAdapter - Dynamsoft Capture Vision Flutter API Reference
description: The class ImageSourceAdapter of Dynamsoft Capture Vision Flutter represents an interface for fetching and buffering images.
keywords: image source adapter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceAdapter

The abstract class `ImageSourceAdapter` is an abstract class for implementing image fetching and delivering features. 

> [!Note]
> Default implementations:
> - [CameraEnhancer]({{ site.dce_flutter_api }}camera-enhancer.html): Use the camera as the image source for scanning from the video input.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
abstract class ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`addImageToBuffer`](#addimagetobuffer) | Adds an image to the internal buffer. |
| [`clearBuffer`](#clearbuffer) | Clears all images from the buffer, resetting the state for new image fetching. |
| [`getBufferOverflowProtectionMode`](#getbufferoverflowprotectionmode) | Get the current mode for handling buffer overflow. |
| [`getColourChannelUsageType`](#getcolourchannelusagetype) | Get the current usage type for color channels in images. |
| [`getImage`](#getimage) | Get a buffered image. Implementing classes should return a Promise that resolves with an instance of `ImageData`. |
| [`getMaximumImageCount`](#getmaximumimagecount) | Get the maximum number of images that can be buffered. |
| [`hasImage`](#hasimage) | Checks if an image with the specified ID is present in the buffer. |
| [`setBufferOverflowProtectionMode`](#setbufferoverflowprotectionmode) | Sets the behavior for handling new incoming images when the buffer is full. |
| [`setColourChannelUsageType`](#setcolourchannelusagetype) | Sets the usage type for color channels in images. |
| [`setMaximumImageCount`](#setmaximumimagecount) | Sets the maximum number of images that can be buffered at any time. |
| [`setNextImageToReturn`](#setnextimagetoreturn) | Sets the processing priority of a specific image. This can affect the order in which images are returned by getImage. |
| [`startFetching`](#startfetching) | Start fetching images from the source to the Video Buffer of `ImageSourceAdapter`. |
| [`stopFetching`](#stopfetching) | Stop fetching images from the source to the Video Buffer of `ImageSourceAdapter`. |

### addImageToBuffer

Adds an image to the internal buffer.

```dart
Future<void> addImageToBuffer(ImageData image);
```

### clearBuffer

Clears all images from the buffer, resetting the state for new image fetching.

```dart
Future<void> clearBuffer();
```

### getBufferOverflowProtectionMode


Get the current mode for handling buffer overflow.

```dart
Future<EnumBufferOverflowProtectionMode> getBufferOverflowProtectionMode() async;
```

### getColourChannelUsageType

Get the current usage type for color channels in images.

```dart
Future<EnumColourChannelUsageType> getColourChannelUsageType();
```

**Remarks**

This method should be used to verify which colour channel the camera is using, and in turn verify what pixel type any images retrieved during the capture process will come out in.

### getImage

Get a buffered image. Implementing classes should return a Promise that resolves with an instance of `ImageData`.

```dart
Future<ImageData?> getImage() async;
```

### getMaximumImageCount

Get the maximum number of images that can be buffered.

```dart
Future<int> getMaximumImageCount();
```

### hasImage

Checks if an image with the specified ID is present in the buffer.

```dart
Future<bool> hasImage(int imageId);
```

### setBufferOverflowProtectionMode

Sets the behavior for handling new incoming images when the buffer is full.

```dart
Future<void> setBufferOverflowProtectionMode(EnumBufferOverflowProtectionMode mode);
```

### setColourChannelUsageType

Sets the usage type for color channels in images.

```dart
Future<void> setColourChannelUsageType(EnumColourChannelUsageType type);
```

**Remarks**

This method should be used to change the pixel type of the original image or captured frame should you choose to retrieve it after the capture process. In order to retrieve the original image after the barcode is decoded or the captured result is received, please refer to [this article].

### setMaximumImageCount

Sets the maximum number of images that can be buffered at any time.

```dart
Future<void> setMaximumImageCount(int count);
```

### setNextImageToReturn

Sets the processing priority of a specific image. This can affect the order in which images are returned by getImage.

```dart
Future<bool> setNextImageToReturn(int imageId, bool keepInBuffer);
```

### startFetching

Start fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

```dart
Future<void> startFetching();
```

### stopFetching

Stop fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

```dart
Future<void> stopFetching();
```

