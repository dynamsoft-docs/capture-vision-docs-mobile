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

> You are viewing a history document page of DynamsoftUtility v1.0.10.

The `DSFileFetcher` class is a utility class that partitions a multi-page image file into multiple independent `ImageData` objects. It inherits from the `DSImageSourceAdapter` class.

## Definition

*Assembly:* DynamsoftUtility.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSFileFetcher : NSObject
```
2. 
```swift
class FileFetcher : NSObject
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
func setFile(withPath filePath: String) throws
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
func setFile(withBytes fileBytes: Data) throws
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
func setFile(withBuffer buffer: ImageData) throws
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
func setFile(withImage image: UIImage) throws
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

### getImage

Get the image data of the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(DSImageData *)getImage;
```
2. 
```swift
func getImage() -> ImageData
```

**Return Value**

A `DSImageData` as the image.
