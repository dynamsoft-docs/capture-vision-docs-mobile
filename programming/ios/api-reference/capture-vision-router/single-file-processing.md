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
`templateName`: Specify a settings template that will be used for the data capturing.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable (The root of sandbox is invalid path for PNG files).

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
`templateName`: Specify a settings template that will be used for data capturing.
`error`: An `NSError` pointer. An error occurs when:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The file path you input is unavailable (The root of sandbox is invalid path for PNGles).

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
`templateName`: Specify a settings template that will be used for data capturing.
`error`: An `NSError` pointer. An error occurs when:

* The method is triggered after the capture is started.
* The template name you input is invalid.
* The image buffer is invalid.

**Return Value**

A [`DSCapturedResult`](../core/basic-structures/captured-result.md) object.

**Code Snippet**

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
let result = try? cvr.captureFromBuffer(data, templateName: name)
```

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
`templateName`: Specify a settings template that will be used for data capturing.
`error`: An `NSError` pointer. An error occurs when:

* The method is triggered after the capture is started.
* The template name you input is invalid.

**Return Value**

A [`DSCapturedResult`](../core/basic-structures/captured-result.md) object.
