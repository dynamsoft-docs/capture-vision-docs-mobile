---
layout: default-layout
Title: DSLicenseManager - Dynamsoft Core Module Android Edition API Reference
Description: The class DSLicenseManager of Dynamsoft Core Module provides a set of APIs to manage SDK licensing.
Keywords: license manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLicenseManager

The `DSLicenseManager` class provides a set of APIs to manage SDK licensing.

## Definition

*Namespace*: com.dynamsoft.license
*Assembly:* DynamsoftLicense.aar

```java
class LicenseManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`initLicense`](#initlicense) | Initialize the license. |
| [`setDeviceFriendlyName`](#setdevicefriendlyname) | Set a human readable name for the device. |
| [`getDeviceUUID`](#getdeviceuuid) |  Get the device UUID. |

### initLicense

Initialize the license.

```java
class func initLicense(_ license: String, verificationDelegate delegate: DSLicenseVerificationListener?)
```

**Parameters**

`license`: A license key.

`delegate`: An delegate object of `DSLicenseVerificationListener` to monitor the license activation status.

### setDeviceFriendlyName

Set a human readable name for the device.

```java
class func setDeviceFriendlyName(_ name: String)
```

**Parameters**

`name`: The name of the device.

### getDeviceUUID

Get the device UUID.

```java
class func getDeviceUUID() -> String
```
