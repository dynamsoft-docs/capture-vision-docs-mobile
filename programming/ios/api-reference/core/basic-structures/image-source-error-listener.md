---
layout: default-layout
title: ImageSourceErrorListener - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The interface ImageSourceErrorListener of Dynamsoft Capture Vision Router Module defines methods for monitoring the errors that occur in the ImageSourceAdapter.
keywords: Error listener, ImageSourceAdapter, objc, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceErrorListener

The `ImageSourceErrorListener` interface that defines methods for monitoring the errors that occur in the [`ImageSourceAdapter`](image-source-adapter.md).

## Definition

*Assembly:* DynamsoftCore.framework

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
- (void)onErrorReceived:( NSError *_Nullable error)imageSourceError;
```
2. 
```swift
func onErrorReceived(_ error: Error)
```
