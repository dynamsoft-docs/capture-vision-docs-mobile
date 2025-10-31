---
layout: default-layout
title: DSImageSourceAdapter - Dynamsoft Core Module iOS Edition API Reference
description: The class DSImageSourceAdapter of Dynamsoft Core Module represents an interface for fetching and buffering images.
keywords: image source adapter, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageSourceAdapter

The `ImageSourceAdapter` class is an abstract class representing an adapter for image sources, providing a framework for fetching, buffering, and managing images from various sources. Implementations must provide specific mechanisms for image retrieval and handling.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSImageSourceAdapter : NSObject
```
2. 
```swift
class ImageSourceAdapter : NSObject
```

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`bufferEmpty`](#bufferempty) | *BOOL* | The read only property determines whether the buffer is currently empty. |
| [`bufferOverflowProtectionMode`](#bufferoverflowprotectionmode) | *DSBufferOverflowProtectionMode* | Sets the behavior for handling new incoming images when the buffer is full. |
| [`colourChannelUsageType`](#colourchannelusagetype) | *colourChannelUsageType* | Sets the usage type for color channels in images. |
| [`imageCount`](#imagecount) | *NSUInteger* | The property defines the current number of images in the buffer. |
| [`maxImageCount`](#maximagecount) | *NSUInteger* | The property defines the maximum number of images that can be buffered. |

| Method | Description |
| ------ | ----------- |
| [`addImageToBuffer`](#addimagetobuffer) | Adds an image to the internal buffer. |
| [`clearBuffer`](#clearbuffer) | Clears all images from the buffer, resetting the state for new image fetching. |
| [`getImage`](#getimage) | Get a buffered image. Implementing classes should return a Promise that resolves with an instance of `DSImageData`. |
| [`hasImage`](#hasimage) | Checks if an image with the specified ID is present in the buffer. |
| [`setErrorListener`](#seterrorlistener) | Sets an error listener to receive notifications about errors that occur during image source operations. |
| [`setImageFetchState`](#setimagefetchstate) | Determines whether there are more images left to fetch. |
| [`setNextImageToReturn`](#setnextimagetoreturn) | Sets the processing priority of a specific image. This can affect the order in which images are returned by `getImage`. |
| [`startFetching`](#startfetching) | Start fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`stopFetching`](#stopfetching) | Stop fetching images from the source to the Video Buffer of ImageSourceAdapter. |

### bufferEmpty

The read only property indicates whether the Video Buffer is empty.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly, getter=isBufferEmpty) BOOL bufferEmpty;
```
2. 
```swift
var isBufferEmpty: Bool { get }
```

### bufferOverflowProtectionMode

Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. You can either block the Video Buffer or push out the oldest image and append a new one.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) DSBufferOverflowProtectionMode bufferOverflowProtectionMode;
```
2. 
```swift
var bufferOverflowProtectionMode:  BufferOverflowProtectionMode { get set }
```

### colourChannelUsageType

The usage type of a color channel in an image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) DSColourChannelUsageType colourChannelUsageType;
```
2. 
```swift
var colourChannelUsageType: ColourChannelUsageType { get set }
```

### hasNextImageToFetch

Determines whether there are more images left to fetch.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) BOOL hasNextImageToFetch;
```
2. 
```swift
var hasNextImageToFetch: Bool { get set }
```

### imageCount

The property defines current image count in the Video Buffer.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly, assign) NSUInteger imageCount;
```
2. 
```swift
var imageCount: Int { get }
```

### maxImageCount

The property defines the maximum capability of the Video Buffer.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSUInteger maxImageCount;
```
2. 
```swift
var maxImageCount: Int { get set }
```

### addImageToBuffer

Adds an image to the internal buffer.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)addImageToBuffer:(DSImageData*)image;
```
2. 
```swift
func addImageToBuffer(image: ImageData)
```

**Parameters**

`[in] image`: The DSImageData object to add.

### clearBuffer

Clears all images from the buffer, resetting the state for new image fetching.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)clearBuffer;
```
2. 
```swift
func clearBuffer()
```

### getImage

Get a buffered image. Implementing classes should return a Promise that resolves with an instance of `DSImageData`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable DSImageData *)getImage;
```
2. 
```swift
func getImage() -> DSImageData?
```

**Return Value**

An object of `DSImageData`.

* If an image is set as the "next image" by method setNextImageToReturn, return that image.
* If no image is set as the "next image", return the latest image.

### hasImage

Checks if an image with the specified ID is present in the buffer.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)hasImage:(NSInteger)imageId;
```
2. 
```swift
func hasImage(imageId: Int) -> Bool
```

**Parameters**

`[in] imageId`: The imageId of image you want to check the availability.

**Return Value**

A BOOL value that indicates whether the specified image is found in the video buffer.

### setErrorListener

Sets an error listener to receive notifications about errors that occur during image source operations.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)setErrorListener:(nullable id<DSImageSourceErrorListener>)listener;
```
2. 
```swift
func setErrorListener(_ listener: ImageSourceErrorListener?)
```

**Parameters**

`[in] listener`: A delegate object of [`DSImageSourceErrorListener`]({{ site.dcv_ios_api }}core/basic-structures/image-source-error-listener.html) to receive the errors that occurs in the `ImageSourceAdapter`.

### setImageFetchState

Determines whether there are more images left to fetch.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)setImageFetchState:(BOOL)state;
```
2. 
```swift
func setImageFetchState(state: Bool)
```

**Parameters**

`[in] state`: The state of image fetching.

### setNextImageToReturn

Sets the processing priority of a specific image. This can affect the order in which images are returned by [`getImage`](#getimage).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)setNextImageToReturn:(NSInteger)imageId
                keepInBuffer:(BOOL)keepInBuffer;
```
2. 
```swift
func setNextImageToReturn(imageId: Int, keepInBuffer: Bool) -> Bool
```

**Parameters**

`[in] imageId`: The imageId of image you want to set as the "next image".  
`[in] keepInBuffer`: Set this value to true so that the "next image" is protected from being pushed out before is it returned by method getImage.

**Return Value**

A BOOL value that indicates whether the specified image is successfully set as the "next image".

### startFetching

Start fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)startFetching;
```
2. 
```swift
func startFetching()
```

### stopFetching

Stop fetching images from the source to the Video Buffer of `ImageSourceAdapter`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)stopFetching;
```
2. 
```swift
func stopFetching()
```
