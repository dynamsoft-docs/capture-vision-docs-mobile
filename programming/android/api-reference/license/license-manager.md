---
layout: default-layout
Title: LicenseManager - Dynamsoft Core Module Android Edition API Reference
Description: The class LicenseManager of Dynamsoft Core Module provides a set of APIs to manage SDK licensing.
Keywords: license manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LicenseManager

The `LicenseManager` class provides a set of APIs to manage SDK licensing.

## Definition

*Namespace:* com.dynamsoft.license
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
static void initLicense(String license, @NonNull Context context, LicenseVerificationListener listener);
```

**Parameters**

`[in] license`: A license key.  

`[in] context`: The context that you want to initialize the license.  

`[in] listener`: An listener object of `LicenseVerificationListener` to monitor the license activation status.

### setDeviceFriendlyName

Set a human readable name for the device.

```java
static void setDeviceFriendlyName(String name);
```

**Parameters**

`[in] name`: The name of the device.

### getDeviceUUID

Get the device UUID.

```java
static String getDeviceUUID(){}
```

**Return Value**

The device UUID.
