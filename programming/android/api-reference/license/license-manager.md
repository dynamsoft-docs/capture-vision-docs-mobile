---
layout: default-layout
title: LicenseManager - Dynamsoft Core Module Android Edition API Reference
description: The class LicenseManager of Dynamsoft Core Module provides a set of APIs to manage SDK licensing.
keywords: license manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---
 
# LicenseManager

The `LicenseManager` class provides a set of APIs to manage SDK licensing.

## Definition

*Namespace:* com.dynamsoft.license

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class LicenseManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`initLicense`](#initlicense) | Initializes the license for the application using a license key. |
| [`setDeviceFriendlyName`](#setdevicefriendlyname) | Assigns a distinctive name to the device, correlating it with its UUID. |
| [`getDeviceUUID`](#getdeviceuuid) | Returns the unique identifier of the device. |
| [`isInitLicenseFinished`](#isinitlicensefinished) | Returns whether the license initialization is finished. |

### initLicense

Initializes the license for the application using a license key.

```java
static void initLicense(final String license, @Nullable final LicenseVerificationListener listener);
```

**Parameters**

`[in] license`: The license key to be used for initialization.

`[in] listener`: A listener object of `LicenseVerificationListener` to monitor the license activation status.

### setDeviceFriendlyName

Assigns a distinctive name to the device, correlating it with its UUID.

```java
static void setDeviceFriendlyName(String name);
```

**Parameters**

`[in] name`: The name of the device.

### getDeviceUUID

Returns the unique identifier of the device.

```java
static String getDeviceUUID(){}
```

**Return Value**

The unique identifier of the device.

### isInitLicenseFinished

Returns whether the license initialization is finished.

```java
static boolean isInitLicenseFinished();
```
