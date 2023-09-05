---
layout: default-layout
title: DSCaptureVisionRouterModule - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class DSCaptureVisionRouterModule of Dynamsoft Capture Vision Router Module represents the capture vision router module, which provides general functions for the capture vision module.
keywords: capture vision, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCaptureVisionRouterModule

The `DSCaptureVisionRouterModule` class defines general functions of the capture vision router module.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCaptureVisionRouterModule : NSObject
```
2. 
```swift
class CaptureVisionRouterModule : NSObject
```

## Methods

| Method | Description |
|------- |-------------|
| [`getVersion`](#getversion) | Get the version of Dynamsoft Capture Vision. |

### getVersion

Get the version of Dynamsoft Capture Vision.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+ (NSString *)getVersion;
```
2. 
```swift
class func getVersion() -> String
```

**Return Value**

The version of Dynamsoft Capture Vision.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSString *version = [DSCaptureVisionRouterModule getVersion];
```
2. 
```swift
let version = CaptureVisionRouterModule.getVersion()
```