---
layout: default-layout
title: DSCoreModule - Dynamsoft Core Module iOS Edition API Reference
description: The class DSCoreModule of Dynamsoft Core Module defines general functions of the core module.
keywords: core module, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
permalink: /programming/ios/api-reference/core/basic-structures/core-module-v2.0.10.html
---

# DSCoreModule

The `DSCoreModule` class defines general functions of the core module.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCoreModule : NSObject
```
2. 
```swift
class CoreModule : NSObject
```

## Methods

| Method | Description |
| ------ |-------------|
| [`getVersion`](#getversion) | Get the version of Dynamsoft Core. |

## getVersion

Get the version of Dynamsoft Core.

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

The version of Dynamsoft Core.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSString *version = [DSCoreModule getVersion];
```
2. 
```swift
let version = CoreModule.getVersion()
```
