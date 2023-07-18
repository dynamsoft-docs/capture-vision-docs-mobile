---
layout: default-layout
Title: DSImageSourceStateListener - Dynamsoft Capture Vision Router Module iOS Edition API Reference
Description: The protocol DSImageSourceStateListener of Dynamsoft Capture Vision Router Module defines methods for monitoring the state of the ImageSourceAdapter.
Keywords: image source state listener, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageSourceStateListener

The `DSImageSourceStateListener` protocol defines methods for monitoring the state of the ImageSourceAdapter.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@protocol DSImageSourceStateListener <NSObject>
```
2. 
```swift
protocol ImageSourceStateListener : NSObject
```

## Methods

| Method | Description |
|------- |-------------|
| [`onImageSourceStateReceived`](#onimagesourcestatereceived) | The methods for monitoring the state of the ImageSourceAdapter. |

### onImageSourceStateReceived

The methods for monitoring the state of the ImageSourceAdapter.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onImageSourceStateReceived:(DSImageSourceState)state;
```
2. 
```swift
func onImageSourceStateReceived(_ state: DSImageSourceState)
```

**Parameters**

`state`: One of the DSImageSourceState that indicates the state of the ImageSourceAdapter.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
[stateListener onImageSourceStateReceived:DSImageSourceStateConnected];
```
2. 
```swift
stateListener.onImageSourceStateReceived(DSImageSourceState.connected)
```
