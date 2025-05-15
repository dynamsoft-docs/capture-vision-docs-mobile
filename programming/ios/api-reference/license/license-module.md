---
layout: default-layout
title: DSLicenseModule - Dynamsoft Core Module iOS Edition API Reference
description: The class DSLicenseModule of Dynamsoft Core Module represents the license module, which provides general functions for managing licenses.
keywords: license module, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLicenseModule

The `DSLicenseModule` class defines common functionality in the `DynamsoftLicense` module.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSLicenseModule : NSObject
```
2. 
```swift
class LicenseModule : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getVersion`](#getversion) | Get the version of `DynamsoftLicense` module. |

## getVersion

Get the version of `DynamsoftLicense` module.

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

The version of `DynamsoftLicense` module.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NSString *version = [DSLicenseModule getVersion];
```
2. 
```swift
let version = LicenseModule.getVersion()
```
