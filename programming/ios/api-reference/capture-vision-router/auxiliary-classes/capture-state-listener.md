---
layout: default-layout
title: DSCaptureStateListener - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The protocol DSCaptureStateListener of Dynamsoft Capture Vision Router Module defines the methods for monitoring the capture state.
keywords: capture state, monitoring, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCaptureStateListener

The `DSCaptureStateListener` protocol defines the methods for monitoring the capture state.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@protocol DSCaptureStateListener <NSObject>
```
2. 
```swift
protocol DSCaptureStateListener : NSObjectProtocol
```

## Methods

| Method | Description |
|------- |-------------|
| [`onCapturedStateChanged`](#oncapturedstatechanged) | The method for monitoring the capture state. |

### onCapturedStateChanged

The method for monitoring the capture state.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onCapturedStateChanged:(DSCaptureState)state;
```
2. 
```swift
func onCapturedStateChanged(_ state: DSCaptureState)
```

**Parameters**

`state`: One of the `DSCaptureState` value that indicates the capture state.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
[self.delegate onCapturedStateChanged:state];
```
2. 
```swift
delegate?.onCapturedStateChanged(state)
```