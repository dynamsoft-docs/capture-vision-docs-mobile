---
layout: default-layout
title: DSLicenseManager - Dynamsoft Core Module iOS Edition API Reference
description: The class DSLicenseManager of Dynamsoft Core Module provides a set of APIs to manage SDK licensing.
keywords: license manager, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLicenseManager

The `DSLicenseManager` class provides a set of APIs to manage SDK licensing.

## Definition

*Assembly:* DynamsoftLicense.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSLicenseManager:NSObject
```
2. 
```swift
class LicenseManager : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`initLicense`](#initlicense) | Initializes the license for the application using a license key. |
| [`setDeviceFriendlyName`](#setdevicefriendlyname) | Assigns a distinctive name to the device, correlating it with its UUID. |
| [`getDeviceUUID`](#getdeviceuuid) |  Get the unique identifier of the device. |

### initLicense

Initializes the license for the application using a license key.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+ (void)initLicense:(NSString* )license verificationDelegate:(id<DSLicenseVerificationListener> _Nullable)delegate;
```
2. 
```swift
class func initLicense(_ license: String, verificationDelegate delegate: DSLicenseVerificationListener?)
```

**Parameters**

`license`: The license key to be used for initialization.

`delegate`: An delegate object of `DSLicenseVerificationListener` to monitor the license activation status.

### setDeviceFriendlyName

Assigns a distinctive name to the device, correlating it with its UUID.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+ (void)setDeviceFriendlyName:(NSString* )name;
```
2. 
```swift
class func setDeviceFriendlyName(_ name: String)
```

**Parameters**

`name`: A string representing the device which is easier to recognize than its UUID.

### getDeviceUUID

Get the unique identifier of the device.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+ (NSString *)getDeviceUUID;
```
2. 
```swift
class func getDeviceUUID() -> String
```

**Return Value**

The unique identifier of the device.
