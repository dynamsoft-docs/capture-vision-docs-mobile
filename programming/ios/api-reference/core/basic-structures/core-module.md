---
layout: default-layout
title: DSCoreModule - Dynamsoft Core Module iOS Edition API Reference
description: The class DSCoreModule of Dynamsoft Core Module defines general functions of the core module.
keywords: core module, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCoreModule

The `DSCoreModule` class defines common functionality in the Core module.

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
| [`getVersion`](#getversion) | Get the version of the `DynamsoftCore` module. |
| [`enableLogging`](#enablelogging) | Enable the output of logs. |
| [`disableLogging`](#disablelogging) | Disable the output of logs. |

## getVersion

Get the version of the `DynamsoftCore` module.

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

The version of the `DynamsoftCore` module.

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

### enableLogging

Enable the output of logs.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+(BOOL)enableLogging:(NSInteger)logMode;
```
2. 
```swift
class func enableLogging(_ logMode:Int)
```

**Parameters**

`logMode`: One of the [`EnumLogMode`]({{ site.dcv_enumerations }}core/log-mode.html?lang=objc&swift) value.

### disableLogging

Disable the output of logs.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+(void)disableLogging;
```
2. 
```swift
class func disableLogging()
```
