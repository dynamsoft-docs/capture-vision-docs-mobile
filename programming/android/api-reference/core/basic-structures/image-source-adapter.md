---
layout: default-layout
Title: ImageSourceAdapter - Dynamsoft Core Module Android Edition API Reference
Description: The class ImageSourceAdapter of Dynamsoft Core Module represents an interface for fetching and buffering images.
Keywords: image source adapter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceAdapter

The `ImageSourceAdapter` class provides an interface for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures
*Assembly:* DynamsoftCore.aar

```java
class ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | Determines whether there are more images left to fetch. |
| [`setMaxImageCount`](#setmaximagecount) | Set the maximum capability of the Video Buffer. |
| [`getMaxImageCount`](#getmaximagecount) | Get the property defines the maximum capability of the Video Buffer. |
| [`setBufferOverflowProtectionMode`](#setbufferoverflowprotectionmode) | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. You can either block the Video Buffer or push out the oldest image and append a new one. |
| [`getBufferOverflowProtectionMode`](#getbufferoverflowprotectionmode) | Get the buffer overflow protection mode. |
| [`getImageCount`](#getimagecount) | Get the current image count in the Video Buffer. |
| [`isBufferEmpty`](#isbufferempty) | Check whether the Video Buffer is empty. |
| [`setColourChannelUsageType`](#setcolourchannelusagetype) | Set the usage type of a color channel in an image. |
| [`getColourChannelUsageType`](#getcolourchannelusagetype) | Get the usage type of a color channel in an image. |
| [`startFetching`](#startfetching) | Start fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`stopFetching`](#stopfetching) | Stop fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`getImage`](#getimage) | Get an image from the Video Buffer. |
| [`setNextImageToReturn(imageId)`](#setnextimagetoreturnimageid) | Specify the next image that is returned by method getImage. |
| [`setNextImageToReturn(imageId,keepInBuffer)`](#setnextimagetoreturnimageidkeepinbuffer) | Specify the next image that is returned by method getImage. |
| [`hasImage`](#hasimage) | Check the availability of the specified image. |
| [`addImageToBuffer`](#addimagetobuffer) | Adds an image to the buffer of the adapter. |
| [`clearBuffer`](#clearbuffer) | Clears the image buffer. |

### hasNextImageToFetch

An abstract method that controls whether there are more images left to fetch.

```java
abstract boolean hasNextImageToFetch();
```

**Return value**

A boolean value that determines whether there are more images left to fetch.

### setMaxImageCount

Set the maximum capability of the Video Buffer.

```java
void setMaximumImageCount(int count);
```

**Parameters**

`count`: The maximum capability of the Video Buffer.

### getMaxImageCount

Get the maximum capability of the Video Buffer.

```java
int getMaximumImageCount();
```

**Return Value**

The maximum capability of the Video Buffer.

### setBufferOverflowProtectionMode

Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. You can either block the Video Buffer or push out the oldest image and append a new one.

```java
void setBufferOverflowProtectionMode(BufferOverflowProtectionMode mode);
```

**Parameters**

`mode`: One of the `EnumBufferOverflowProtectionMode` that indicates the buffer overflow protection mode.

### getBufferOverflowProtectionMode

Get the buffer overflow protection mode.

```java
BufferOverflowProtectionMode getBufferOverflowProtectionMode();
```

**Return Value**

The buffer overflow protection mode.

### getImageCount

Get the current image count in the Video Buffer.

```java
int getImageCount();
```

### isBufferEmpty

Check whether the Video Buffer is empty.

```java
boolean isBufferEmpty();
```

**Return Value**

A boolean value that indicates whether the Video Buffer is empty.

### setColourChannelUsageType

The usage type of a color channel in an image.

```java
void setColourChannelUsageType(EnumColourChannelUsageType type);
```

**Parameters**

`type`: One of the `EnumColourChannelUsageType` that indicates whether the colour channel usage type.

### getColourChannelUsageType

The usage type of a color channel in an image.

```java
EnumColourChannelUsageType getColourChannelUsageType();
```

**Return Value**

One of the `EnumColourChannelUsageType` that indicates whether the colour channel usage type.

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

### getImage

Get an image from the Video Buffer.

```java
ImageData getImage();
```

**Return Value**

An object of ImageData.

* If an image is set as the "next image" by method `setNextImageToReturn`, return that image.
* If no image is set as the "next image", return the latest image.

### setNextImageToReturn(imageId)

Specify the next image that is returned by method getImage.

```java
boolean setNextImageToReturn(int imageId);
```

**Parameters**

`imageId`: The imageId of image you want to set as the "next image".  

**Return Value**

A boolean value that indicates whether the specified image is successfully set as the "next image".

### setNextImageToReturn(imageId,keepInBuffer)

Specify the next image that is returned by method getImage.

```java
boolean setNextImageToReturn(int imageId, boolean keepInBuffer)
```

**Parameters**

`imageId`: The imageId of image you want to set as the "next image".  
`keepInBuffer`: Set this value to true so that the "next image" is protected from being pushed out before is it returned by method getImage.

**Return Value**

A boolean value that indicates whether the specified image is successfully set as the "next image".

### hasImage

Check the availability of the specified image.

```java
boolean hasImage(int imageId);
```

**Parameters**

`imageId`: The imageId of image you want to check the availability.

**Return Value**

A boolean value that indicates whether the specified image is found in the video buffer.

### addImageToBuffer

Adds an image to the buffer of the adapter.

```java
void addImageToBuffer(ImageData image);
```

**Parameters**

`image`: The ImageData object to add.

### clearBuffer

Clears the image buffer.

```java
void clearBuffer();
```
