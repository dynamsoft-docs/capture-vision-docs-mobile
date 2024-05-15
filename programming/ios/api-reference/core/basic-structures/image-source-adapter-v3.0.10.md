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

The `DSImageSourceAdapter` class provides an interface for fetching and buffering images. It is an abstract class that needs to be implemented by a concrete class to provide actual functionality.

## Definition

*Assembly:* DynamsoftCore.framework

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

## Methods & Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | *BOOL* |Determines whether there are more images left to fetch. |
| [`maxImageCount`](#maximagecount) | *NSUInteger* | The property defines the maximum capability of the Video Buffer. |
| [`bufferOverflowProtectionMode`](#bufferoverflowprotectionmode) | *DSBufferOverflowProtectionMode* | Sets a mode that determines the action to take when there is a new incoming image and the buffer is full. You can either block the Video Buffer or push out the oldest image and append a new one. |
| [`imageCount`](#imagecount) | *NSUInteger* | The property defines current image count in the Video Buffer. |
| [`bufferEmpty`](#bufferempty) | *BOOL* | The read only property indicates whether the Video Buffer is empty. |
| [`colourChannelUsageType`](#colourchannelusagetype) | *colourChannelUsageType* | The usage type of a color channel in an image. |

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
var bufferOverflowProtectionMode: DSBufferOverflowProtectionMode { get set }
```

### imageCount

The property defines current image count in the Video Buffer.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSUInteger imageCount;
```
2. 
```swift
var imageCount: Int { get set }
```

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
var bufferEmpty: Bool { get }
```

### colourChannelUsageType

The usage type of a color channel in an image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) colourChannelUsageType;
```
2. 
```swift
var colourChannelUsageType: colourChannelUsageType { get set }
```

### startFetching

Start fetching images from the source to the Video Buffer of ImageSourceAdapter.

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

Stop fetching images from the source to the Video Buffer of ImageSourceAdapter.

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

### getImage

Get an image from the Video Buffer.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *_Nullable)getImage;
```
2. 
```swift
func getImage() -> DSImageData?
```

**Return Value**

An object of DSImageData.

* If an image is set as the "next image" by method setNextImageToReturn, return that image.
* If no image is set as the "next image", return the latest image.

### setNextImageToReturn

Specify the next image that is returned by method getImage.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)setNextImageToReturn:(NSInteger)imageId;
```
2. 
```swift
func setNextImageToReturn(imageId: Int) -> Bool
```

**Parameters**

`[in] imageId`: The imageId of image you want to set as the "next image".  
`[in] keepInBuffer`: Set this value to true so that the "next image" is protected from being pushed out before is it returned by method getImage.

**Return Value**

A BOOL value that indicates whether the specified image is successfully set as the "next image".

### hasImage

Check the availability of the specified image.

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

### addImageToBuffer

Adds an image to the buffer of the adapter.

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
func addImageToBuffer(image: DSImageData)
```

**Parameters**

`[in] image`: The DSImageData object to add.

### clearBuffer

Clears the image buffer.

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

## setErrorListener

Registers a [`ImageSourceErrorListener`](image-source-error-listener.md) to be used as a callback when an error occurs in the `ImageSourceAdapter`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)setErrorListener:(DSImageSourceErrorListener)listener;
```
2. 
```swift
func setErrorListener(_ listener:ImageSourceErrorListener)
```

**Parameters**

`[in] listener`: A delegate object of [`DSImageSourceErrorListener`](auxiliary-classes/capture-state-listener.md) to receive the errors that occurs in the `ImageSourceAdapter`.
