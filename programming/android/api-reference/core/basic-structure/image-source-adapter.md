---
layout: default-layout
Title: DSImageSourceAdapter - Dynamsoft Core Module Android Edition API Reference
Description: The class DSImageSourceAdapter of Dynamsoft Core Module represents an interface for fetching and buffering images.
Keywords: image source adapter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageSourceAdapter

The `DSImageSourceAdapter` class provides an interface for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class ImageSourceAdapter
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | *BOOL* |Determines whether there are more images left to fetch. |
| [`maxImageCount`](#maximagecount) | *NSUInteger* | The property defines the maximum capability of the Video Buffer. |
| [`bufferOverflowProtectionMode`](#bufferoverflowprotectionmode) | *DSBufferOverflowProtectionMode* | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. You can either block the Video Buffer or push out the oldest image and append a new one. |
| [`imageCount`](#imagecount) | *NSUInteger* | The property defines current image count in the Video Buffer. |
| [`bufferEmpty`](#bufferempty) | *BOOL* | The read only property indicates whether the Video Buffer is empty. |
| [`colourChannelUsageType`](#colourchannelusagetype) | *colourChannelUsageType* | The usage type of a color channel in an image. |

## Methods

| Method | Description |
| ------ | ----------- |
| [`startFetching`](#startfetching) | Start fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`stopFetching`](#stopfetching) | Stop fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`getImage`](#getimage) | Get an image from the Video Buffer. |
| [`setNextImageToReturn`](#setnextimagetoreturn) | Specify the next image that is returned by method getImage. |
| [`hasImage`](#hasimage) | Check the availability of the specified image. |
| [`addImageToBuffer`](#addimagetobuffer) | Adds an image to the buffer of the adapter. |
| [`clearBuffer`](#clearbuffer) | Clears the image buffer. |

### hasNextImageToFetch

Determines whether there are more images left to fetch.

```java
var hasNextImageToFetch: Bool { get set }
```

### maxImageCount

The property defines the maximum capability of the Video Buffer.

```java
var maxImageCount: Int { get set }
```

### bufferOverflowProtectionMode

Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. You can either block the Video Buffer or push out the oldest image and append a new one.

```java
var bufferOverflowProtectionMode: DSBufferOverflowProtectionMode { get set }
```

### imageCount

The property defines current image count in the Video Buffer.

```java
var imageCount: Int { get set }
```

### bufferEmpty

The read only property indicates whether the Video Buffer is empty.

```java
var bufferEmpty: Bool { get }
```

### colourChannelUsageType

The usage type of a color channel in an image.

```java
var colourChannelUsageType: colourChannelUsageType { get set }
```

### startFetching

Start fetching images from the source to the Video Buffer of ImageSourceAdapter.

```java
func startFetching()
```

### stopFetching

Stop fetching images from the source to the Video Buffer of ImageSourceAdapter.

```java
func stopFetching()
```

### getImage

Get an image from the Video Buffer.

```java
func getImage() -> DSImageData?
```

**Return Value**

An object of DSImageData.

* If an image is set as the "next image" by method setNextImageToReturn, return that image.
* If no image is set as the "next image", return the latest image.

### setNextImageToReturn

Specify the next image that is returned by method getImage.

```java
func setNextImageToReturn(imageId: Int) -> Bool
```

**Parameters**

`[in] imageId`: The imageId of image you want to set as the "next image".  
`[in] keepInBuffer`: Set this value to true so that the "next image" is protected from being pushed out before is it returned by method getImage.

**Return Value**

A BOOL value that indicates whether the specified image is successfully set as the "next image".

### hasImage

Check the availability of the specified image.

```java
func hasImage(imageId: Int) -> Bool
```

**Parameters**

`[in] imageId`: The imageId of image you want to check the availability.

**Return Value**

A BOOL value that indicates whether the specified image is found in the video buffer.

### addImageToBuffer

Adds an image to the buffer of the adapter.

```java
func addImageToBuffer(image: DSImageData)
```

**Parameters**

`[in] image`: The DSImageData object to add.

### clearBuffer

Clears the image buffer.

```java
func clearBuffer()
```
