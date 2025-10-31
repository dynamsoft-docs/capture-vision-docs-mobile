---
layout: default-layout
title: ImageSourceAdapter - Dynamsoft Core Module Android Edition API Reference
description: The class ImageSourceAdapter of Dynamsoft Core Module represents an interface for fetching and buffering images.
keywords: image source adapter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceAdapter

The `ImageSourceAdapter` class provides an interface for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`ImageSourceAdapter`](#imagesourceadapter-1 ) | The constructor. |
| [`addImageToBuffer`](#addimagetobuffer) | Adds an image to the internal buffer. |
| [`clearBuffer`](#clearbuffer) | Clears all images from the buffer, resetting the state for new image fetching. |
| [`getBufferOverflowProtectionMode`](#getbufferoverflowprotectionmode) | Get the current mode for handling buffer overflow. |
| [`getColourChannelUsageType`](#getcolourchannelusagetype) | Get the current usage type for color channels in images. |
| [`getImageCount`](#getimagecount) | Get the current number of images in the buffer. |
| [`getImage`](#getimage) | Get a buffered image. Implementing classes should return a Promise that resolves with an instance of `DSImageData`. |
| [`getMaxImageCount`](#getmaximagecount) | Get the maximum number of images that can be buffered. |
| [`hasImage`](#hasimage) | Checks if an image with the specified ID is present in the buffer. |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | Determines whether there are more images available to fetch. |
| [`isBufferEmpty`](#isbufferempty) | Determines whether the buffer is currently empty. |
| [`setBufferOverflowProtectionMode`](#setbufferoverflowprotectionmode) | Sets the behavior for handling new incoming images when the buffer is full. |
| [`setColourChannelUsageType`](#setcolourchannelusagetype) | Sets the usage type for color channels in images. |
| [`setErrorListener`](#seterrorlistener) | Sets an error listener to receive notifications about errors that occur during image source operations. |
| [`setMaxImageCount`](#setmaximagecount) | Sets the maximum number of images that can be buffered at any time. |
| [`setNextImageToReturn(imageId)`](#setnextimagetoreturnimageid) | Sets the processing priority of a specific image. This can affect the order in which images are returned by getImage. |
| [`setNextImageToReturn(imageId,keepInBuffer)`](#setnextimagetoreturnimageidkeepinbuffer) | Sets the processing priority of a specific image. This can affect the order in which images are returned by getImage. |
| [`startFetching`](#startfetching) | Start fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`stopFetching`](#stopfetching) | Stop fetching images from the source to the Video Buffer of ImageSourceAdapter. |

### ImageSourceAdapter

The constructor.

```java
ImageSourceAdapter();
```

### addImageToBuffer

Adds an image to the internal buffer.

```java
void addImageToBuffer(ImageData image);
```

**Parameters**

`[in] image`: The ImageData object to add.

### clearBuffer

Clears all images from the buffer, resetting the state for new image fetching.

```java
void clearBuffer();
```

### getBufferOverflowProtectionMode

Get the current mode for handling buffer overflow.

```java
@EnumBufferOverflowProtectionMode
int getBufferOverflowProtectionMode();
```

### getColourChannelUsageType

Get the current usage type for color channels in images.

```java
@EnumColourChannelUsageType
int getColourChannelUsageType();
```

### getImageCount

Get the current number of images in the buffer.

```java
int getImageCount();
```

**Return Value**

The current number of images in the buffer.

### getImage

Get an image from the Video Buffer.

```java
ImageData getImage();
```

**Return Value**

An object of ImageData.

* If an image is set as the "next image" by method `setNextImageToReturn`, return that image.
* If no image is set as the "next image", return the latest image.

### getMaxImageCount

Get the maximum number of images that can be buffered.

```java
int getMaximumImageCount();
```

**Return Value**

The maximum capability of the Video Buffer.

### hasImage

Checks if an image with the specified ID is present in the buffer.

```java
boolean hasImage(int imageId);
```

**Parameters**

`[in] imageId`: The imageId of image you want to check the availability.

**Return Value**

A boolean value that indicates whether the specified image is found in the video buffer.

### hasNextImageToFetch

Determines whether there are more images available to fetch.

```java
abstract boolean hasNextImageToFetch();
```

**Return value**

A boolean value that determines whether there are more images left to fetch.

### isBufferEmpty

Determines whether the buffer is currently empty.

```java
boolean isBufferEmpty();
```

**Return Value**

A boolean value that indicates whether the Video Buffer is empty.

### setBufferOverflowProtectionMode

Sets the behavior for handling new incoming images when the buffer is full.

```java
void setBufferOverflowProtectionMode(@EnumBufferOverflowProtectionMode int mode);
```

**Parameters**

`[in] mode`: One of the `EnumBufferOverflowProtectionMode` that indicates the buffer overflow protection mode.

**Return Value**

The buffer overflow protection mode.

### setColourChannelUsageType

Sets the usage type for color channels in images.

```java
void setColourChannelUsageType(@EnumColourChannelUsageType int type);
```

**Parameters**

`[in] type`: One of the [`EnumColourChannelUsageType`]({{ site.dcv_android_api }}core/enum/colour-channel-usage-type.html) that indicates whether the colour channel usage type.

**Return Value**

One of the [`EnumColourChannelUsageType`]({{ site.dcv_android_api }}core/enum/colour-channel-usage-type.html) that indicates whether the colour channel usage type.

### setErrorListener

Sets an error listener to receive notifications about errors that occur during image source operations.

```java
void setErrorListener(ImageSourceErrorListener listener);
```

**Parameters**

`[in] listener`: A interface object of [`ImageSourceErrorListener`](image-source-error-listener.md) to receive the errors that occurs in the `ImageSourceAdapter`.

### setMaxImageCount

Sets the maximum number of images that can be buffered at any time.

```java
void setMaximumImageCount(int count);
```

**Parameters**

`[in] count`: The maximum capability of the Video Buffer.

### setNextImageToReturn(imageId)

Sets the processing priority of a specific image. This can affect the order in which images are returned by getImage.

```java
boolean setNextImageToReturn(int imageId);
```

**Parameters**

`[in] imageId`: The imageId of image you want to set as the "next image".  

**Return Value**

A boolean value that indicates whether the specified image is successfully set as the "next image".

### setNextImageToReturn(imageId,keepInBuffer)

Sets the processing priority of a specific image. This can affect the order in which images are returned by getImage.

```java
boolean setNextImageToReturn(int imageId, boolean keepInBuffer)
```

**Parameters**

`[in] imageId`: The imageId of image you want to set as the "next image".  

`[in] keepInBuffer`: Set this value to true so that the "next image" is protected from being pushed out before is it returned by method getImage.

**Return Value**

A boolean value that indicates whether the specified image is successfully set as the "next image".

### startFetching

Start fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

```java
void startFetching();
```

### stopFetching

Stop fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

```java
void stopFetching();
```
