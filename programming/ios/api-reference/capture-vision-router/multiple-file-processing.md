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
| [`addImageSourceStateListener`](#addimagesourcestatelistener) | Regisiter a DSImageSourceStateListener to get callback when the status of DSImageSourceAdapter changes. |
| [`removeImageSourceStateListener`](#removeimagesourcestatelistener) | Remove a DSImageSourceStateListener. |
| [`addResultReceiver`](#addresultreceiver) | Regisiter a DSCapturedResultReceiver to get callback when DSCapturedResult output. |
| [`removeResultReceiver`](#removeresultreceiver) | Remove a DSCapturedResultReceiver. |
| [`startCapturing`](#startcapturing) | Start capturing with the targeting template. |
| [`stopCapturing`](#stopcapturing) | Start capturing with the targeting template. |
| [`addCaptureStateListener`](#addcapturestatelistener) | Regisiter a DSCaptureStateListener to get callback when capture state changes. |
| [`removeCaptureStateListener`](#removecapturestatelistener) | Remove a DSCaptureStateListener. |
| [`addResultFilter`](#addresultfilter) | Regisiter a DSCapturedResultFilter to get callback when filtered result output. |
| [`removeResultFilter`](#removeresultfilter) | Remove a DSCapturedResultFilter. |

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

Regisiter a `DSImageSourceStateListener` to get callback when the status of `DSImageSourceAdapter` changes.

**Parameters**

`listener`: An object of `DSImageSourceStateListener`.
`error`: An NSError pointer. An error occurs if the method is triggered after the capture is started.

**Return Value**

A bool value that indicates whether the `DSImageSourceStateListener` is added successfully.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)addImageSourceStateListener:(id<DSImageSourceStateListener>)listener
                              error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func addImageSourceStateListener(_ listener:DSImageSourceStateListener) throws -> BOOL
```

## removeImageSourceStateListener

Remove a `DSImageSourceStateListener`.

**Parameters**

`listener`: An object of `DSImageSourceStateListener`.
`error`: An NSError pointer. An error occurs if the method is triggered after the capture is started.

**Return Value**

A bool value that indicates whether the `DSImageSourceStateListener` is removed successfully.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeImageSourceStateListener:(id<DSImageSourceStateListener>)listener
                                 error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func removeImageSourceStateListener(_ listener:DSImageSourceStateListener) throws -> BOOL
```

## addResultReceiver

Regisiter a `DSCapturedResultReceiver` to get callback when `DSCapturedResult` output.

**Parameters**

`listener`: An object of `DSCapturedResultReceiver`.
`error`: An NSError pointer. An error occurs if the method is triggered after the capture is started.

**Return Value**

A bool value that indicates whether the result receiver is added successfully.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)addResultReceiver:(id<DSCapturedResultReceiver>)receiver
                    error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func addResultReceiver(_ listener:DSCapturedResultReceiver) throws -> BOOL
```

## removeResultReceiver

Remove a `DSCapturedResultReceiver`.

**Parameters**

`listener`: An object of `DSCapturedResultReceiver`.
`error`: An NSError pointer. An error occurs if the method is triggered after the capture is started.

**Return Value**

A bool value that indicates whether the result receiver is removed successfully.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeResultReceiver:(id<DSCapturedResultReceiver>)receiver
                       error:(NSError * _Nullable * _Nullable)error;
```
2. 
```swift
func removeResultReceiver(_ listener:DSCapturedResultReceiver) throws -> BOOL
```

## startCapturing

Start capturing with the targeting template.

**Parameters**

`templateName`: The name of a template that you have previously set via `initSettings` or `initSettingsFromFile`.
`error`: An NSError pointer. An error occurs when:

* The method is triggered after the capture is started.
* Your templateName is invalid.
* Your image source is invalid.

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

Regisiter a `DSCaptureStateListener` to get callback when capture state changes.

**Parameters**

`listener`: A delegate object of `DSCaptureStateListener` to receive the capture state.
`error`: An NSError pointer. An error occurs if the method is triggered after the capture is started.

**Return Value**

A BOOL value that indicates whether the capture state listener is added successfully.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)addCaptureStateListener:(nonnull id<DSCaptureStateListener>)listener
                          error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func addCaptureStateListener(_ listener:DSCaptureStateListener) throws -> BOOL
```

## removeCaptureStateListener

Remove a `DSCaptureStateListener`.

**Parameters**

`listener`: An object of `DSCaptureStateListener`.
`error`: An NSError pointer. An error occurs if the method is triggered after the capture is started.

**Return Value**

A BOOL value that indicates whether the capture state listener is removed successfully.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeCaptureStateListener:(nonnull id<DSCaptureStateListener>)listener
                             error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func removeCaptureStateListener(_ listener:DSCaptureStateListener) throws -> BOOL
```

## addResultFilter

Regisiter a `DSCapturedResultFilter` to get callback when filtered result output.

**Parameters**

`filter`: An object of `DSCapturedResultFilter`.
`error`: An NSError pointer. An error occurs if the method is triggered after the capture is started.

**Return Value**

A BOOL value that indicates whether the result filter is added successfully.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)addResultFilter:(nonnull id<DSCapturedResultFilter>)filter
                          error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func addResultFilter(_ filter:DSCapturedResultFilter) throws -> BOOL
```

## removeResultFilter

Remove a `DSCapturedResultFilter`.

**Parameters**

`filter`: An object of `DSCapturedResultFilter`.
`error`: An NSError pointer. An error occurs if the method is triggered after the capture is started.

**Return Value**

A BOOL value that indicates whether the result filter is removed successfully.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)removeResultFilter:(nonnull id<DSCapturedResultFilter>)filter
                             error:(NSError * _Nullable * _Nullable)error
```
2. 
```swift
func removeResultFilter(_ filter:DSCapturedResultFilter) throws -> BOOL
```
