---
layout: default-layout
Title: Processing a Single Image - Dynamsoft Capture Vision Router Module iOS Edition API Reference
Description: The APIs of the DSCaptureVisionRouter for processing a single image.
Keywords: capture vision, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing a Single Image

| Method | Description |
| ------ | ----------- |
| [`captureFromFile`](#capturefromfile) | Capture data from the file specified by the file path. |
| [`captureFromFileBytes`](#capturefromfilebytes) | Capture data from a given file in memory. |
| [`captureFromBuffer`](#capturefrombuffer) | Capture data from the memory buffer via a `DSImageData` object. |
| [`captureFromImage`](#capturefromimage) | Capture data from the given image. |

## captureFromFile

Capture data from the file specified by the file path. To learn more about what the captured data can be, please see the *Return Value* section below.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable DSCapturedResult *)captureFromFile:(NSString *)file
                                  templateName:(nonnull NSString*)templateName
                                         error:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func captureFromFile(_ file:String, templateName:String) throws -> CaptureResult
```

**Parameters**

`file`: The file path and name that you want to capture data from.  
`templateName`: Specify a template with a templateName for the data capturing.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

**Return Value**

A [`DSCapturedResult`](../core/basic-structures/captured-result.md) object.

## captureFromFileBytes

Capture data from a given file in memory. To learn more about what the captured data can be, please see the *Return Value* section below.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable DSCapturedResult *)captureFromFileBytes:(NSData *)fileBytes
                                                  templateName:(nonnull NSString*)templateName
                                                         error:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func captureFromFileBytes(_ fileBytes:Data, templateName:String) throws -> CaptureResult
```

**Parameters**

`fileBytes`: A `NSData` object that points to a file in memory.  
`templateName`: Specify a template with a templateName for the data capturing.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

**Return Value**

A [`DSCapturedResult`](../core/basic-structures/captured-result.md) object.

## captureFromBuffer

Capture data from the memory buffer via a `DSImageData` object. To learn more about what the captured data can be, please see the *Return Value* section below.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable DSCapturedResult *)captureFromBuffer:(DSImageData *)buffer
                                    templateName:(nonnull NSString*)templateName
                                           error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func captureFromBuffer(_ buffer:DSImageData, templateName:String) throws -> CaptureResult
```

**Parameters**

`buffer`: A [`DSImageData`](../core/basic-structures/image-data.md) object that contains image info.  
`templateName`: Specify a template with a templateName for the data capturing.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

**Return Value**

A [`DSCapturedResult`](../core/basic-structures/captured-result.md) object.

## captureFromImage

Capture data from the given image. To learn more about what the captured data can be, please see the *Return Value* section below.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable DSCapturedResult *)captureFromImage:(UIImage *)image
                                    templateName:(nonnull NSString*)templateName
                                            error:(NSError *_Nullable *_Nullable)error;
```
2. 
```swift
func captureFromBuffer(_ image:UIImage, templateName:String) throws -> CaptureResult
```

**Parameters**

`image`: A `UIImage` object.  
`templateName`: Specify a template with a templateName for the data capturing.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

**Return Value**

A [`DSCapturedResult`](../core/basic-structures/captured-result.md) object.
