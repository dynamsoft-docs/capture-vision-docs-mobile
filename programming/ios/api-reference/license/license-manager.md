---
layout: default-layout
Title: DSLicenseManager - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSLicenseManager of Dynamsoft Core Module provides a set of APIs to manage SDK licensing.
Keywords: license manager, objective-c, swift
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
| [`initLicense`](#initlicense) | Initialize the license. |
| [`setDeviceFriendlyName`](#setdevicefriendlyname) | Set a human readable name for the device. |
| [`getDeviceUUID`](#getdeviceuuid) |  Get the device UUID. |

### initLicense

Initialize the license.

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

`license`: A license key.

`delegate`: An delegate object of `DSLicenseVerificationListener` to monitor the license activation status.

### setDeviceFriendlyName

Set a human readable name for the device.

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

`name`: The name of the device.

### getDeviceUUID

Get the device UUID.

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

