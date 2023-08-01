---
layout: default-layout
Title: DSFileFetcher - Dynamsoft Capture Vision Router Module iOS Edition API Reference
Description: The class DSFileFetcher of Dynamsoft Capture Vision Router Module is a utility class that partitions a multi-page image file into multiple independent ImageData objects.
Keywords: file fetcher, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSFileFetcher

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
| [`setPDFReadingParameter`](#setpdfreadingparameter) | Sets the parameters of PDF reading. |
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

`[in,out] error`: An `NSError` pointer. An error occurs when fail to load the image.

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

`[in,out] error`: An `NSError` pointer. An error occurs when fail to load the image.

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

`[in,out] error`: An `NSError` pointer. An error occurs when fail to load the image.

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

`[in,out] error`: An `NSError` pointer. An error occurs when fail to load the image.

### setPDFReadingParameter

Sets the parameters of PDF reading.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(BOOL)setPDFReadingParameter:(PDFReadingParameter *)para
                        error:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func setPDFReadingParameter(_ para: PDFReadingParameter) throws
```
**Parameters**

`para`: The parameter object for reading PDF files.

`[in,out] error`: An `NSError` pointer. An error occurs when:
- The directory is unavailable.
- The method is triggered after the capture is started.

**Return Value**

A BOOL value that indicates whether the PDF reading mode is set successfully.

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
