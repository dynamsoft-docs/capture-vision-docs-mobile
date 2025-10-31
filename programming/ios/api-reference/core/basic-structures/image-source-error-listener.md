---
layout: default-layout
title: ImageSourceErrorListener - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The protocol ImageSourceErrorListener of Dynamsoft Capture Vision Router Module defines methods for monitoring the errors that occur in the ImageSourceAdapter.
keywords: Error listener, ImageSourceAdapter, objc, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceErrorListener

The `ImageSourceErrorListener` protocol defines methods for monitoring the errors that occur in the [`ImageSourceAdapter`](image-source-adapter.md).

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@protocol DSImageSourceErrorListener <NSObject>
```
2. 
```swift
protocol ImageSourceErrorListener: NSObjectProtocol
```

## Methods

| Method | Description |
|------- |-------------|
| [`onErrorReceived`](#onerrorreceived) | The callback method for monitoring the errors that occur in the [`ImageSourceAdapter`](image-source-adapter.md). |

### onErrorReceived

The callback method for monitoring the errors that occur in the [`ImageSourceAdapter`](image-source-adapter.md).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onErrorReceived:(NSError *)error;
```
2. 
```swift
func onErrorReceived(_error: Error)
```

**Parameters**

`error`: An NSError containing the error code and error message providing the information about the error.
