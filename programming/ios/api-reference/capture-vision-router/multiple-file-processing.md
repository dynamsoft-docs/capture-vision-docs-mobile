---
layout: default-layout
Title: Processing multiple Images/Pages - Dynamsoft Capture Vision Router Module iOS Edition API Reference
Description: The APIs of the DSCaptureVisionRouter for processing multiple Images/Pages.
Keywords: capture vision, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Processing multiple Images/Pages

| Method | Description |
| ------ | ----------- |
| [`setInput`](#setinput) | Sets an image source to provide images for consecutive process. |
| [`getInput`](#getinput) | Gets the attached image source adapter object of the capture vision router. |
| [`addImageSourceStateListener`](#addimagesourcestatelistener) | Registers a DSImageSourceStateListener to get callback when the status of DSImageSourceAdapter changes. |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Removes a DSImageSourceStateListener. |
| [`addResultReceiver`](#addresultreceiver) | Registers a DSCapturedResultReceiver to get callback when DSCapturedResult output. |
| [`removeResultReceiver`](#removeresultreceiver) | Removes a DSCapturedResultReceiver. |
| [`startCapturing`](#startcapturing) | Start capturing with the targeting template. |
| [`stopCapturing`](#stopcapturing) | Start capturing with the targeting template. |
| [`addCaptureStateListener`](#addcapturestatelistener) | Registers a DSCaptureStateListener to get callback when capture state changes. |
| [`removeCaptureStateListener`](#removecapturestatelistener) | Removes a DSCaptureStateListener. |
| [`addResultFilter`](#addresultfilter) | Registers a DSCapturedResultFilter to get callback when filtered result output. |
| [`removeResultFilter`](#removeresultfilter) | Removes a DSCapturedResultFilter. |

## setInput

Sets an image source to provide images for consecutive process.

**Parameters**

`adapter`: An object of `DSImageSourceAdapter`. You can use a internally implemented `ImageSourceAdapter` such as `CameraEnhancer`, `DirectoryFetcher` and `FileFetcher`.
`error`: An NSError pointer. An error occurs if the method is triggered after the capture is started.

**Return Value**

A bool value that indicates whether the input is set successfully.

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

Gets the attached image source adapter object of the capture vision router.

**Return Value**

The attached image source adapter object of the capture vision router.

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

Registers a `DSImageSourceStateListener` to get callback when the status of `DSImageSourceAdapter` changes.

**Parameters**

`listener`: An object of `DSImageSourceStateListener`.

**Return Value**

A bool value that indicates whether the `DSImageSourceStateListener` is added successfully.

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

Removes a `DSImageSourceStateListener`.

**Parameters**

`listener`: An object of `DSImageSourceStateListener`.

**Return Value**

A bool value that indicates whether the `DSImageSourceStateListener` is removed successfully.

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

Registers a `DSCapturedResultReceiver` to get callback when `DSCapturedResult` output.

**Parameters**

`listener`: An object of `DSCapturedResultReceiver`.

**Return Value**

A bool value that indicates whether the result receiver is added successfully.

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

Removes a `DSCapturedResultReceiver`.

**Parameters**

`listener`: An object of `DSCapturedResultReceiver`.

**Return Value**

A bool value that indicates whether the result receiver is removed successfully.

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

Start capturing with the targeting template.

**Parameters**

`templateName`: The name of a template that you have previously set via `initSettings` or `initSettingsFromFile`.

**Return Value**

A bool value that indicates whether the capture starts successfully.

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
func removeResultReceiver(_ templateName:String) throws -> BOOL
```

## stopCapturing

Stop capturing.

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

Registers a `DSCaptureStateListener` to get callback when capture state changes.

**Parameters**

`listener`: A delegate object of `DSCaptureStateListener` to receive the capture state.

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

Removes a `DSCaptureStateListener`.

**Parameters**

`listener`: An object of `DSCaptureStateListener`.

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

Registers a `DSCapturedResultFilter` to get callback when filtered result output.

**Parameters**

`filter`: An object of `DSCapturedResultFilter`.

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

Removes a `DSCapturedResultFilter`.

**Parameters**

`filter`: An object of `DSCapturedResultFilter`.

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
