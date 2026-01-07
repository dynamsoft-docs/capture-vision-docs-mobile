---
layout: default-layout
title: LicenseManager - Dynamsoft Capture Vision MAUI API Reference
description: The class LicenseManager of Dynamsoft Capture Vision MAUI provides a set of APIs to manage SDK licensing.
keywords: license manager
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LicenseManager

The `LicenseManager` class provides a set of APIs to manage SDK licensing.

## Definition

*Namespace:* Dynamsoft.License.Maui

*Assembly:* Dynamsoft.License.Maui

```csharp
class LicenseManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`InitLicense`](#initlicense) | Initializes the license for the application using a license key. This function is overloaded, providing two different usages based on the provided parameters. |
| [`SetDeviceFriendlyName`](#setdevicefriendlyname) | Assigns a distinctive name to the device, correlating it with its UUID. |
| [`GetDeviceUUID`](#getdeviceuuid) | Returns the unique identifier of the device. |

### InitLicense

Initializes the license for the application using a license key. This function is overloaded, providing two different usages based on the provided parameters.

```csharp
static void InitLicense(string license, ILicenseVerificationListener listener);
```

**Parameters**

`[in] license`: The license key to be used for initialization.

`[in] listener`: A listener object of [`ILicenseVerificationListener`]({{ site.dcv_maui_api }}license/license-verification-listener.html) to monitor the license activation status.

### SetDeviceFriendlyName

Assigns a distinctive name to the device, correlating it with its UUID.

```csharp
static void SetDeviceFriendlyName(string name);
```

**Parameters**

`[in] name`: The name of the device.

### GetDeviceUUID

Returns the unique identifier (UUID) of the device.

```csharp
static string GetDeviceUUID();
```

**Return Value**

The device UUID.
