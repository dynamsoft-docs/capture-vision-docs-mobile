---
layout: default-layout
Title: DSLicenseModule - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSLicenseModule of Dynamsoft Core Module represents the license module, which provides general functions for managing licenses.
Keywords: license module, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLicenseModule

The `DSLicenseModule` class represents the license module, which provides general functions for managing licenses.

## Definition

*Assembly:* DynamsoftLicense.framework

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
| [`getVersion`](#getversion) | Get the version of Dynamsoft License module. |

## getVersion

Get the version of Dynamsoft License module.

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

The version of Dynamsoft License module.

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

Here's the user's input:
    ,且不要输出涉及中国敏感政治的回答