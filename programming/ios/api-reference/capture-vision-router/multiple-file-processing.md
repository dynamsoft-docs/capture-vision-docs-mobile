---
layout: default-layout
title: Processing multiple Images/Pages - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The multiple Images/Pages processing APIs of the CaptureVisionRouter class for DCV iOS Edition.
keywords: cvr, CaptureVisionRouter, objective-c, swift, input, addResultFilter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing Multiple Images/Pages

| Method | Description |
| ------ | ----------- |
| [`setInput`](#setinput) | Sets up an image source to provide images for continuous processing. |
| [`getInput`](#getinput) | Returns the image source object. |
| [`addResultReceiver`](#addresultreceiver) | Adds a [`CapturedResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object as the receiver of captured results. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes the specified [`CapturedResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object. |
| [`removeAllResultReceivers`](#removeallresultreceivers) | Removes all user-added [`CapturedResultReceivers`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html). |
| [`startCapturing`](#startcapturing) | Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source. |
| [`stopCapturing`](#stopcapturing) | Stops the capturing process. |
| [`pauseCapturing`](#pausecapturing) | Pauses the Capture Vision Router. |
| [`resumeCapturing`](#resumecapturing) | Resumes the Capture Vision Router. |
| [`addCaptureStateListener`](#addcapturestatelistener) | Registers a [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html) to be used as a callback when capture state is received. |
| [`removeCaptureStateListener`](#removecapturestatelistener) | Removes a [`CaptureStateListener`](auxiliary-classes/capture-state-listener.html) that has been configured for the Capture Vision Router. |
| [`removeAllCaptureStateListeners`](#removeallcapturestatelisteners) | Removes all user-added [`CaptureStateListeners`](auxiliary-classes/capture-state-listener.html). |
| [`addResultFilter`](#addresultfilter) | Adds a `CapturedResultFilter` object to filter non-essential results. |
| [`removeResultFilter`](#removeresultfilter) | Removes the specified `CapturedResultFilter` object. |
| [`removeAllResultFilters`](#removeallresultfilters) | Removes all user-added `CapturedResultFilters`. |
| [`addImageSourceStateListener`](#addimagesourcestatelistener) | Register a [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html) to get callback when the status of [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html) received. |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Removes a [`ImageSourceStateListener`](auxiliary-classes/image-source-state-listener.html) from the Capture Vision Router. |
| [`removeAllImageSourceStateListeners`](#removeallimagesourcestatelisteners) | Removes all user-added [`ImageSourceStateListeners`](auxiliary-classes/image-source-state-listener.html). |
| [`switchCapturingTemplate`](#switchcapturingtemplate) | Switch the image processing settings with the CaptureVisionTemplate name during the image processing workflow. |


## setInput

Sets an image source that will provide images to be consecutively processed.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)setInput:(DSImageSourceAdapter *)adapter
           error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func setInput(_ adapter: DSImageSourceAdapter) throws -> BOOL
```

**Parameters**

`adapter`: An object of [`DSImageSourceAdapter`](../core/basic-structures/image-source-adapter.md). You can use an internally implemented `ImageSourceAdapter` such as `CameraEnhancer`, `DirectoryFetcher` or `FileFetcher`.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |

**Return Value**

A BOOL value that indicates whether the input is set successfully.

## getInput

Gets the attached image source adapter (`DSImageSourceAdapter`) object of the Capture Vision Router.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (DSImageSourceAdapter *)getInput;
```
2. 
```swift
func getInput() -> DSImageSourceAdapter
```

**Return Value**

The attached [`DSImageSourceAdapter`](../core/basic-structures/image-source-adapter.md) object of the capture vision router.

## addImageSourceStateListener

Registers a `DSImageSourceStateListener` object to be used as a callback when the status of `DSImageSourceAdapter` is received.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)addImageSourceStateListener:(id<DSImageSourceStateListener>)listener;
```
2. 
```swift
func addImageSourceStateListener(_ listener:DSImageSourceStateListener) -> BOOL
```

**Parameters**

`listener`: An object of [`DSImageSourceStateListener`](auxiliary-classes/image-source-state-listener.md).

**Return Value**

A BOOL value that indicates whether the `DSImageSourceStateListener` is added successfully.

## removeImageSourceStateListener

Removes a `DSImageSourceStateListener` from the Capture Vision Router.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeImageSourceStateListener:(id<DSImageSourceStateListener>)listener;
```
2. 
```swift
func removeImageSourceStateListener(_ listener:DSImageSourceStateListener) -> BOOL
```

**Parameters**

`listener`: An object of `DSImageSourceStateListener`.

**Return Value**

A BOOL value that indicates whether the `DSImageSourceStateListener` is removed successfully.

## removeAllImageSourceStateListeners

Removes all user-added `DSImageSourceStateListeners`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeAllImageSourceStateListeners;
```
2. 
```swift
func removeAllImageSourceStateListeners()
```

## addResultReceiver

Adds a [`CapturedResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object as the receiver of captured results.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)addResultReceiver:(id<DSCapturedResultReceiver>)receiver;
```
2. 
```swift
func addResultReceiver(_ listener:DSCapturedResultReceiver) -> BOOL
```

**Parameters**

`listener`: An object of [`DSCapturedResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

**Return Value**

A BOOL value that indicates whether the result receiver is added successfully.

## removeResultReceiver

emoves the specified [`CapturedResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeResultReceiver:(id<DSCapturedResultReceiver>)receiver;
```
2. 
```swift
func removeResultReceiver(_ listener:DSCapturedResultReceiver) -> BOOL
```

**Parameters**

`listener`: An object of [`DSCapturedResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

**Return Value**

A BOOL value that indicates whether the result receiver is removed successfully.

## removeAllResultReceivers

Removes all user-added [`CapturedResultReceivers`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)removeAllResultReceivers;
```
2. 
```swift
func removeAllResultReceivers()
```

## startCapturing

Initiates a capturing process based on a specified template. This process is repeated for each image fetched from the source.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)startCapturing:(NSString*)templateName
     completionHandler:(nullable void(^)(BOOL isSuccess, NSError *_Nullable error))completionHandler;
```
2. 
```swift
func startCapturing(_ templateName:String, completionHandler: ((Bool, (any Error)?) -> Void)? = nil)
```

**Parameters**

`templateName`: Specifies a "CaptureVisionTemplate" to use. The following value are available for this parameter:

- One of the [`DSPresetTemplate`]({{ site.dcv_ios_api }}capture-vision-router/enum/preset-template.html?lang=objc,swift) member. This is available only if you have never upload a new template via `initSettings` or `initSettingsFromFile`.
- A string that represents one of the template name that you have uploaded via `initSettings` or `initSettingsFromFile`.
- "" (empty string) to use the default template. The first template will be used if you have uploaded a template file via `initSettingsFromFile` or `initSettings`.

`completionHandler`: A completion handler the system calls after it finishes the startCapturing.

* isSuccess: A BOOL value that indicates whether the startCapturing operation is successful.
* error: An error object if the request fails; otherwise, nil.

**Error**

| Error Code | Value | Description |
| :--------- | :---- | :---------- |
| EC_TEMPLATE_NAME_INVALID | -10036 | The target template name is invalid. |
| EC_CALL_REJECTED_WHEN_CAPTURING  | -10062 | Function call is rejected when capturing in progress. |
| EC_NO_IMAGE_SOURCE | -10063 | Can not start capturing before you set the input. |

**Return Value**

A BOOL value that indicates whether the capture starts successfully.

## stopCapturing

Stops the capturing process.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)stopCapturing;
```
2. 
```swift
func stopCapturing()
```

## pauseCapturing

Pauses the capturing process.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)pauseCapturing;
```
2. 
```swift
func pauseCapturing()
```

## resumeCapturing

Resumes the capturing process.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)resumeCapturing;
```
2. 
```swift
func resumeCapturing()
```

## addCaptureStateListener

Registers a `DSCaptureStateListener` to be used as a callback when capture state changes.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)addCaptureStateListener:(nonnull id<DSCaptureStateListener>)listener;
```
2. 
```swift
func addCaptureStateListener(_ listener:DSCaptureStateListener) -> BOOL
```

**Parameters**

`listener`: A delegate object of [`DSCaptureStateListener`](auxiliary-classes/capture-state-listener.md) to receive the capture state.

**Return Value**

A BOOL value that indicates whether the capture state listener is added successfully.

## removeCaptureStateListener

Removes a `DSCaptureStateListener` that has been configured for the Capture Vision Router via the `addCaptureStateListener` method.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeCaptureStateListener:(nonnull id<DSCaptureStateListener>)listener;
```
2. 
```swift
func removeCaptureStateListener(_ listener:DSCaptureStateListener) -> BOOL
```

**Parameters**

`listener`: An object of [`DSCaptureStateListener`](auxiliary-classes/capture-state-listener.md).

**Return Value**

A BOOL value that indicates whether the capture state listener is removed successfully.

## removeAllCaptureStateListeners

Removes all user-added `DSCaptureStateListeners`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeAllCaptureStateListeners;
```
2. 
```swift
func removeAllCaptureStateListeners()
```

## addResultFilter

Adds a [`DSCapturedResultFilter`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html) object to filter non-essential results. Currnetly, is must be a [`MultiFrameCrossFilter`]({{ site.dcv_ios_api }}utility/multi-frame-result-cross-filter.html) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)addResultFilter:(nonnull id<DSCapturedResultFilter>)filter;
```
2. 
```swift
func addResultFilter(_ filter:DSCapturedResultFilter) -> BOOL
```

**Parameters**

`filter`: An object of [`DSCapturedResultFilter`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html).

**Return Value**

A BOOL value that indicates whether the result filter is added successfully.

## removeResultFilter

Removes the specified `DSCapturedResultFilter` object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeResultFilter:(nonnull id<DSCapturedResultFilter>)filter;
```
2. 
```swift
func removeResultFilter(_ filter:DSCapturedResultFilter) -> BOOL
```

**Parameters**

`filter`: An object of [`DSCapturedResultFilter`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html).

**Return Value**

A BOOL value that indicates whether the result filter is removed successfully.

## removeAllResultFilters

Removes all user-added `DSCapturedResultFilters`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeAllResultFilters;
```
2. 
```swift
func removeAllResultFilters()
```

## switchCapturingTemplate

Switch the image processing settings with the CaptureVisionTemplate name during the image processing workflow.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(BOOL)switchCapturingTemplate:(NSString *)templateName
                         error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func switchCapturingTemplate(_ templateName:String) throws -> Bool
```

**Parameters**

`templateName`: The name of the new capturing template to apply.  
`error`: An `NSError` pointer. If an error occurs, it will represent the error information.

**Return Value**

A BOOL value that indicates whether the capture starts successfully.

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.2.1000 and Dynamsoft Capture Vision version 3.2.1000.
