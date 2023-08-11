---
layout: default-layout
Title: Processing multiple Images/Pages - Dynamsoft Capture Vision Router Module iOS Edition API Reference
Description: The APIs of the DSCaptureVisionRouter for processing multiple Images/Pages.
Keywords: capture vision, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing Multiple Images/Pages

| Method | Description |
| ------ | ----------- |
| [`setInput`](#setinput) | Sets an image source that will provide images to be consecutively processed. |
| [`getInput`](#getinput) | Gets the attached image source adapter object of the Capture Vision Router. |
| [`addImageSourceStateListener`](#addimagesourcestatelistener) | Registers a `DSImageSourceStateListener` object to be used as a callback when the status of `DSImageSourceAdapter` changes. |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Removes a `DSImageSourceStateListener` from the Capture Vision Router. |
| [`addResultReceiver`](#addresultreceiver) | Registers a result receiver to be used as a callback when the library outputs a captured result. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes a result receiver from the Capture Vision Router. |
| [`startCapturing`](#startcapturing) | Start capturing with the specified template. |
| [`stopCapturing`](#stopcapturing) | Tells the Capture Vision Router to stop capturing. |
| [`addCaptureStateListener`](#addcapturestatelistener) | Registers a `DSCaptureStateListener` to be used as a callback when capture state changes. |
| [`removeCaptureStateListener`](#removecapturestatelistener) | Removes a `DSCaptureStateListener` that has been configured for the Capture Vision Router. |
| [`addResultFilter`](#addresultfilter) | Registers a `DSCapturedResultFilter` to be used as a callback when the Capture Vision Router outputs filtered result(s). |
| [`removeResultFilter`](#removeresultfilter) | Removes a `DSCapturedResultFilter` that has been configured for the Capture Vision Router. |

## setInput

Sets an image source that will provide images to be consecutively processed.

**Parameters**

`adapter`: An object of [`DSImageSourceAdapter`](../core/basic-structures/image-source-adapter.md). You can use an internally implemented `ImageSourceAdapter` such as `CameraEnhancer`, `DirectoryFetcher` or `FileFetcher`.
`error`: An `NSError` pointer. An error occurs if the method is triggered after the capture starts.

**Return Value**

A BOOL value that indicates whether the input is set successfully.


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

## getInput

Gets the attached image source adapter (`DSImageSourceAdapter`) object of the Capture Vision Router.

**Return Value**

The attached [`DSImageSourceAdapter`](../core/basic-structures/image-source-adapter.md) object of the capture vision router.

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
func getInput() throws -> DSImageSourceAdapter
```

## addImageSourceStateListener

Registers a `DSImageSourceStateListener` object to be used as a callback when the status of `DSImageSourceAdapter` is received.

**Parameters**

`listener`: An object of [`DSImageSourceStateListener`](auxiliary-classes/image-source-state-listener.md).

**Return Value**

A BOOL value that indicates whether the `DSImageSourceStateListener` is added successfully.

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

## removeImageSourceStateListener

Removes a `DSImageSourceStateListener` from the Capture Vision Router.

**Parameters**

`listener`: An object of `DSImageSourceStateListener`.

**Return Value**

A BOOL value that indicates whether the `DSImageSourceStateListener` is removed successfully.

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

## addResultReceiver

Registers a `DSCapturedResultReceiver` to be used as a callback when the library outputs a `DSCapturedResult`.

**Parameters**

`listener`: An object of [`DSCapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md).

**Return Value**

A BOOL value that indicates whether the result receiver is added successfully.

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

## removeResultReceiver

Removes a `DSCapturedResultReceiver` from the Capture Vision Router.

**Parameters**

`listener`: An object of [`DSCapturedResultReceiver`](../core/basic-structures/captured-result-receiver.md).

**Return Value**

A BOOL value that indicates whether the result receiver is removed successfully.

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

## startCapturing

Start capturing with the specified template.

**Parameters**

`templateName`: The name of a template that you have previously set via [`initSettings`](settings.md#initsettings) or [`initSettingsFromFile`](settings.md#initsettingsfromfile).

**Return Value**

A BOOL value that indicates whether the capture starts successfully.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)startCapturing:(NSString*)templateName
                 error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func startCapturing(_ templateName:String) throws -> BOOL
```

## stopCapturing

Tells the Capture Vision Router to stop capturing.

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

## addCaptureStateListener

Registers a `DSCaptureStateListener` to be used as a callback when capture state changes.

**Parameters**

`listener`: A delegate object of [`DSCaptureStateListener`](auxiliary-classes/capture-state-listener.md) to receive the capture state.

**Return Value**

A BOOL value that indicates whether the capture state listener is added successfully.

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

## removeCaptureStateListener

Removes a `DSCaptureStateListener` that has been configured for the Capture Vision Router via the `addCaptureStateListener` method.

**Parameters**

`listener`: An object of [`DSCaptureStateListener`](auxiliary-classes/capture-state-listener.md).

**Return Value**

A BOOL value that indicates whether the capture state listener is removed successfully.

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

## addResultFilter

Registers a `DSCapturedResultFilter` to be used as a callback when the Capture Vision Router outputs filtered result(s).

**Parameters**

`filter`: An object of [`DSCapturedResultFilter`](../core/basic-structures/captured-result-filter.md).

**Return Value**

A BOOL value that indicates whether the result filter is added successfully.

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

## removeResultFilter

Removes a `DSCapturedResultFilter` that has been configured for the Capture Vision Router via the `addResultFilter` method.

**Parameters**

`filter`: An object of [`DSCapturedResultFilter`](../core/basic-structures/captured-result-filter.md).

**Return Value**

A BOOL value that indicates whether the result filter is removed successfully.

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
