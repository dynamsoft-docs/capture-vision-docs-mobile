---
layout: default-layout
title: Processing a Single Image - Dynamsoft Capture Vision iOS API Reference
description: The APIs of the DSCaptureVisionRouter for processing a single image.
keywords: capture vision, objective-c, swift
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
| [`captureMultiPagesFromFile`](#capturemultipagesfromfile) | Capture data from a multi-page file specified by the file path. |
| [`captureMultiPagesFromFileBytes`](#capturemultipagesfromfilebytes) | Capture data from a multi-page file in memory. |
| [`captureMultiPagesFromFileFetcher`](#capturemultipagesfromfilefetcher) | Capture data from a multi-page file via a `DSFileFetcher`. |

## captureFromFile

Capture data from the file specified by the file path. To learn more about what the captured data can be, please see the *Return Value* section below.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSCapturedResult *)captureFromFile:(NSString *)file
                         templateName:(NSString*)templateName;
```
2. 
```swift
func captureFromFile(_ file:String, templateName:String) -> CaptureResult
```

**Parameters**

`file`: The file path and name that you want to capture data from.

`templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`DSPresetTemplate`]({{ site.dcv_ios_api }}capture-vision-router/enum/preset-template.html?lang=objc,swift) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

A [`DSCapturedResult`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result.html) object.

If an error occurs when processing the image, the `DSCapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_FILE_NOT_FOUND | -10005 | The file is not found. |
| EC_FILE_TYPE_NOT_SUPPORTED | -10006 | The file type is not supported. |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## captureFromFileBytes

Capture data from a given file in memory. To learn more about what the captured data can be, please see the *Return Value* section below.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSCapturedResult *)captureFromFileBytes:(NSData *)fileBytes
                              templateName:(NSString*)templateName;
```
2. 
```swift
func captureFromFileBytes(_ fileBytes:Data, templateName:String) -> CaptureResult
```

**Parameters**

`fileBytes`: A `NSData` object that points to a file in memory.

`templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`DSPresetTemplate`]({{ site.dcv_ios_api }}capture-vision-router/enum/preset-template.html?lang=objc,swift) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

A [`DSCapturedResult`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result.html) object.

If an error occurs when processing the image, the `DSCapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## captureFromBuffer

Capture data from the memory buffer via a `DSImageData` object. To learn more about what the captured data can be, please see the *Return Value* section below.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSCapturedResult *)captureFromBuffer:(DSImageData *)buffer
                           templateName:(NSString*)templateName;
```
2. 
```swift
func captureFromBuffer(_ buffer:DSImageData, templateName:String) -> CaptureResult
```

**Parameters**

`buffer`: A [`DSImageData`](../core/basic-structures/image-data.md) object that contains image info.

`templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`DSPresetTemplate`]({{ site.dcv_ios_api }}capture-vision-router/enum/preset-template.html?lang=objc,swift) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

A [`DSCapturedResult`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result.html) object.

If an error occurs when processing the image, the `DSCapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_NULL_POINTER | -10002 | The ImageData object is null. |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## captureFromImage

Capture data from the given image. To learn more about what the captured data can be, please see the *Return Value* section below.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSCapturedResult *)captureFromImage:(UIImage *)image
                          templateName:(NSString*)templateName;
```
2. 
```swift
func captureFromImage(_ image:UIImage, templateName:String) -> CaptureResult
```

**Parameters**

`image`: A `UIImage` object.

`templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`DSPresetTemplate`]({{ site.dcv_ios_api }}capture-vision-router/enum/preset-template.html?lang=objc,swift) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

A [`DSCapturedResult`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result.html) object.

If an error occurs when processing the image, the `DSCapturedResult` object will include error code and error message that describes the reason of the error.

Possible errors:

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TIMEOUT | -10026 | The processing timeout. If not all the tasks are timeout, you will still receive the results of the processed tasks. |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_MULTI_PAGES_NOT_SUPPORTED | -10066 | The api does not support multi-page files. Please use FileFetcher instead. |

## captureMultiPagesFromFile

Capture data from a multi-page file specified by the file path.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSArray<DSCapturedResult *> *)captureMultiPagesFromFile:(NSString *)file
                                              templateName:(NSString *)templateName;
```
2. 
```swift
func captureMultiPagesFromFile(_ file: String, templateName: String) -> [CapturedResult]
```

**Parameters**

`file`: The file path and name that you want to capture data from.

`templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`DSPresetTemplate`]({{ site.dcv_ios_api }}capture-vision-router/enum/preset-template.html?lang=objc,swift) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

An array of [`DSCapturedResult`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result.html) objects.

## captureMultiPagesFromFileBytes

Capture data from a multi-page file in memory.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSArray<DSCapturedResult *> *)captureMultiPagesFromFileBytes:(NSData *)fileBytes
                                                   templateName:(NSString *)templateName;
```
2. 
```swift
func captureMultiPagesFromFileBytes(_ fileBytes: Data, templateName: String) -> [CapturedResult]
```

**Parameters**

`fileBytes`: A `NSData` object that points to a file in memory.

`templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`DSPresetTemplate`]({{ site.dcv_ios_api }}capture-vision-router/enum/preset-template.html?lang=objc,swift) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

An array of [`DSCapturedResult`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result.html) objects.

## captureMultiPagesFromFileFetcher

Capture data from a multi-page file via a [`DSFileFetcher`]({{ site.dcv_ios_api }}utility/file-fetcher.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSArray<DSCapturedResult *> *)captureMultiPagesFromFileFetcher:(DSFileFetcher *)fetcher
                                                     templateName:(NSString *)templateName;
```
2. 
```swift
func captureMultiPagesFromFileFetcher(_ fetcher: FileFetcher, templateName: String) -> [CapturedResult]
```

**Parameters**

`fetcher`: A [`DSFileFetcher`]({{ site.dcv_ios_api }}utility/file-fetcher.html) object.

`templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`DSPresetTemplate`]({{ site.dcv_ios_api }}capture-vision-router/enum/preset-template.html?lang=objc,swift) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

**Return Value**

An array of [`DSCapturedResult`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result.html) objects.
