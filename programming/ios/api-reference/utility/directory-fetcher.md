---
layout: default-layout
title: DSDirectoryFetcher - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class DSDirectoryFetcher of Dynamsoft Capture Vision Router Module is a utility class that retrieves a list of files from a specified directory based on certain criteria.
keywords: directory fetcher, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSDirectoryFetcher

The `DSDirectoryFetcher` class is a utility class that retrieves a list of files from a specified directory based on certain criteria. It inherits from the `DSProactiveImageSourceAdapter` class.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(DirectoryFetcher)
@interface DSDirectoryFetcher : DSProactiveImageSourceAdapter
```
2. 
```swift
class DirectoryFetcher : ProactiveImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`init`](#init) | Create an instance of DSDirectoryFetcher. |
| [`setDirectory`](#setdirectory) | Sets the directory path and filter for the file search. |
| [`setPages`](#setpages) | Set the pages to read. |

The following methods are inherited from [`DSProactiveImageSourceAdapter`]({{ site.dcv_ios_api }}core/basic-structures/proactive-image-source-adapter.html).

| Method | Description |
| ------ | ----------- |
| [`setImageFetchInterval`]({{ site.dcv_ios_api }}core/basic-structures/proactive-image-source-adapter.html#setimagefetchinterval) | Sets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer. |
| [`getImageFetchInterval`]({{ site.dcv_ios_api }}core/basic-structures/proactive-image-source-adapter.html#getimagefetchinterval) | Gets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer. |

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

### init

Create an instance of DSDirectoryFetcher.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)init;
```
2. 
```swift
init()
```

**Return Value**

An instance of `DSDirectoryFetcher`.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
DSDirectoryFetcher *fetcher = [[DSDirectoryFetcher alloc] init];
```
2. 
```swift
let fetcher = DirectoryFetcher()
```

### setDirectory

Sets the directory path and filter for the file search.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)setDirectory:(NSString *)directoryPath
              filter:(NSString *)filter
           recursive:(BOOL)recursive
               error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func setDirectory(_ directoryPath: String, filter: String?, recursive: Bool) throws
```

**Parameters**

`directoryPath`: The directory path.

`filter`: A string that specifies file extensions. It determines which kinds of files to read. e.g "\*.BMP;\*.JPG;\*.GIF".

`recursive`: Specifies whether to load files recursively.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_READ_DIRECTORY_FAILED | -10064 | Failed to read the directory. |

**Return Value**

A `BOOL` value that indicates whether the directory is set successfully.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSError *error;
BOOL success = [fetcher setDirectory:directoryPath filter:nil recursive:YES error:&error];
```
2. 
```swift
do {
   try fetcher.setDirectory(directoryPath, filter: nil, recursive: true)
} catch {
   // Add your code to deal with exceptions.
}
```

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
