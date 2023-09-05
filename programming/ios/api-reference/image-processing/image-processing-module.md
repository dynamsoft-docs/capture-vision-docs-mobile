---
layout: default-layout
title: DSImageProcessingModule - Dynamsoft Image Processing Module iOS Edition API Reference
description: The class DSImageProcessingModule of Dynamsoft Image Processing Module represents general functions of the image processing module.
keywords: image processing module, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageProcessingModule

The `DSImageProcessingModule` class defines general functions of the image processing module.

## Definition

*Assembly:* DynamsoftImageProcessing.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSImageProcessingModule : NSObject
```
2. 
```swift
class ImageProcessingModule : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getVersion`](#getversion) | Get the version of Dynamsoft Image Processing module. |

### getVersion

Get the version of Dynamsoft Image Processing module.

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

The version of Dynamsoft Image Processing module.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSString *version = [DSImageProcessingModule getVersion];
```
2. 
```swift
let version = ImageProcessingModule.getVersion()
```
