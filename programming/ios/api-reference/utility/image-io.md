---
layout: default-layout
title: ImageIO - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class ImageIO of Dynamsoft Capture Vision Router Module is a utility class for managing the image data. It provides functionality for saving images to files and reading images from files.
keywords: image io, image manager, Objective-C, OC, Swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageIO

The class `ImageIO` is a utility class for managing the image data. It provides functionality for saving images to files and reading images from files.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSImageIO : NSObject
```
2. 
```swift
class ImageIO : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`readFromFile`](#readfromfile) | Reads an image from the specified path and format. |
| [`readFromMemory`](#readfrommemory) | Reads an image from the memory. |
| [`saveToFile`](#savetofile) | Saves an image to the specified path and format. |
| [`saveToMemory`](#savetomemory) | Saves an image to the memory. |

```objc
/**
 * Reads an image from a file.
 * @param [in] filePath The path of the image file.
 * @param [in,out] error An NSError pointer.
 *
 * @return Returns a DSImageData object representing the image.
 */
- (DSImageData *)readFromFile:(NSString *)filePath
                        error:(NSError * _Nullable * _Nullable)error;

/**
 * Reads an image from a file in memory.
 * @param [in] fileBytes A NSData object that points to a file in memory.
 * @param [in,out] error An NSError pointer.
 *
 * @return Returns a DSImageData object representing the image.
 */
- (DSImageData *)readFromMemory:(NSData *)fileBytes
                          error:(NSError * _Nullable * _Nullable)error;


```

### saveToFile

Saves an image to the specified path and format. The desired file format is inferred from the file extension provided in the `path` parameter.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)saveToFile:(DSImageData *)imageData
              path:(NSString *)path
         overWrite:(BOOL)overWrite
             error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func save(toFile imageData: ImageData, path: String, overWrite: Bool) throws -> Bool
```

**Parameters**

`imageData`: The image to be saved, of type `ImageData`.

`path`: The file path, name and extension name, as a string, under which the image will be saved.

`overWrite`: A flag indicating whether to overwrite the file if it already exists. Defaults to true.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_FILE_ALREADY_EXISTS | -10067 | The file already exists but overwriting is disabled. |
| EC_CREATE_FILE_FAILED | -10068 | The file path does not exist but cannot be created, or the file cannot be created for any other reason. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

**Return Value**

A `BOOL` value that indicates whether the file is saved successfully.

### saveToMemory

Saves an image to the memory.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSData *)saveToMemory:(DSImageData *)imageData
             imageFormat:(DSImageFileFormat)imageFormat
                   error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func saveToMemory(imageData: ImageData, imageFormat: ImageFileFormat) throws -> Data
```

**Parameters**

`imageData`: The image to be saved, of type `ImageData`.

`imageFormat`: The image format.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Return Value**

The image bytes.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_IMGAE_DATA_INVALID | -10069 | The input ImageData object contains invalid parameter(s). |

### readFromFile

Reads an image from the specified path and format.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)readFromFile:(NSString *)filePath
                        error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func readFromFile(filePath: String) throws -> ImageData
```

**Parameters**

`filePath`: The file path, name and extension name, as a string, from which the image will be read.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Return Value**

The image data of type `ImageData`.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |

### readFromMemory

Reads an image from the memory.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageData *)readFromMemory:(NSData *)fileBytes
                          error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func readFromMemory(fileBytes: Data) throws -> ImageData
```

**Parameters**

`fileBytes`: The image bytes.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Return Value**

The image data of type `ImageData`.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The fileBytes you input is null. |
