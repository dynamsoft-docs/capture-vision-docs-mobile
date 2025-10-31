---
layout: default-layout
title: DSFileFetcher - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class DSFileFetcher of Dynamsoft Capture Vision Router Module is a utility class that partitions a multi-page image file into multiple independent ImageData objects.
keywords: file fetcher, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSFileFetcher

The `DSFileFetcher` class is a utility class that partitions a multi-page image file into multiple independent `ImageData` objects. It inherits from the `DSImageSourceAdapter` class.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSFileFetcher : DSImageSourceAdapter
```
2. 
```swift
class FileFetcher : DSImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`setFileWithPath`](#setfilewithpath) | Sets the file with a file path. |
| [`setFileWithBytes`](#setfilewithbytes) | Sets the file with file bytes. |
| [`setFileWithBuffer`](#setfilewithbuffer) | Sets the file with a `DSImageData` object. |
| [`setFileWithImage`](#setfilewithimage) | Sets the file with a `UIImage`. |
| [`hasNextImageToFetch`](#hasnextimagetofetch) | Whether there is a next image to fetch. |
| [`getImage`](#getimage) | Get the image data of the image. |
| [`setPages`](#setpages) | Set the pages to read. |

The following methods & attributes are inherited from [`DSImageSourceAdapter`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html).

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`bufferEmpty`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#bufferempty) | *BOOL* | The read only property determines whether the buffer is currently empty. |
| [`bufferOverflowProtectionMode`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#bufferoverflowprotectionmode) | *DSBufferOverflowProtectionMode* | Sets the behavior for handling new incoming images when the buffer is full. |
| [`colourChannelUsageType`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#colourchannelusagetype) | *colourChannelUsageType* | Sets the usage type for color channels in images. |
| [`hasNextImageToFetch`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#hasnextimagetofetch) | *BOOL* | Determines whether there are more images available to fetch. |
| [`imageCount`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#imagecount) | *NSUInteger* | The property defines the current number of images in the buffer. |
| [`maxImageCount`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#maximagecount) | *NSUInteger* | The property defines the maximum number of images that can be buffered. |

| Method | Description |
| ------ | ----------- |
| [`addImageToBuffer`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#addimagetobuffer) | Adds an image to the internal buffer. |
| [`clearBuffer`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#clearbuffer) | Clears all images from the buffer, resetting the state for new image fetching. |
| [`getImage`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#getimage) | Get a buffered image. Implementing classes should return a Promise that resolves with an instance of `DSImageData`. |
| [`hasImage`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#hasimage) | Checks if an image with the specified ID is present in the buffer. |
| [`setErrorListener`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#seterrorlistener) | Sets an error listener to receive notifications about errors that occur during image source operations. |
| [`setNextImageToReturn`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#setnextimagetoreturn) | Sets the processing priority of a specific image. This can affect the order in which images are returned by `getImage`. |
| [`startFetching`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#startfetching) | Start fetching images from the source to the Video Buffer of ImageSourceAdapter. |
| [`stopFetching`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#stopfetching) | Stop fetching images from the source to the Video Buffer of ImageSourceAdapter. |

### setFileWithPath

Sets the file with a file path.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(BOOL)setFileWithPath:(NSString *)filePath
                 error:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func setFileWithPath( _filePath: String) throws
```

**Parameters**

`filePath`: The file path.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |

### setFileWithBytes

Sets the file with file bytes.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(BOOL)setFileWithBytes:(NSData *)fileBytes
                  error:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func setFileWithBytes( _fileBytes: Data) throws
```

**Parameters**

`fileBytes`: The file bytes.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The fileBytes you input is null. |

### setFileWithBuffer

Sets the file with a `DSImageData` object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(BOOL)setFileWithBuffer:(DSImageData *)buffer
                   error:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func setFileWithBuffer( _buffer: ImageData) throws
```
**Parameters**

`buffer`: The image data.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The fileBytes you input is null. |

### setFileWithImage

Sets the file with a `UIImage`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(BOOL)setFileWithImage:(UIImage *)image
                  error:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func setFileWithImage( _image: UIImage) throws
```
**Parameters**

`image`: A `UIImage`.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The fileBytes you input is null. |

### hasNextImageToFetch

Whether there is a next image to fetch.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(BOOL)hasNextImageToFetch;
```
2. 
```swift
func hasNextImageToFetch() -> Bool
```

**Return Value**

A bool value that indicates whether there is a next image to fetch.

### setPages

Set the pages to read.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(BOOL)setPages:(NSArray<NSNumber *> *)pages
          error:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func setPages(_ pages: NSArray) throws -> BOOL
```

**Parameters**

`pages`: An array that contains all the pages to read.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND  | -10005 | File not found. |
| EC_FILE_TYPE_NOT_SUPPORTED  | -10006 | The file type is not supported. |
| EC_IMAGE_READ_FAILED  | -10012 | Failed to read the image. |
