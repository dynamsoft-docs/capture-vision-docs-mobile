---
layout: default-layout
title: DSUtilityModule - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class DSUtilityModule of Dynamsoft Capture Vision Router Module represents general functions of the utility module.
keywords: utility module, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSUtilityModule

The `DSUtilityModule` class defines common functionality in the `DynamsoftUtility` module.

## Definition

*Assembly:* DynamsoftUtility.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSUtilityModule : NSObject
```
2. 
```swift
class UtilityModule : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getVersion`](#getversion) | Get the version of `DynamsoftUtility` module. |

## getVersion

Get the version of `DynamsoftUtility` module.

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

The version of `DynamsoftUtility` module.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSString *version = [DSUtilityModule getVersion];
```
2. 
```swift
let version = UtilityModule.getVersion()
```