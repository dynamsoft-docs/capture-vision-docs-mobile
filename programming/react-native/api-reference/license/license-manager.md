---
layout: default-layout
title: LicenseManager Class - Dynamsoft Capture Vision React Native
description: LicenseManager class of DCV React Native provides API to initialize and verify product licenses.
keywords: license, manager, barcode reader, react native, capture vision
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LicenseManager

The `LicenseManager` class provides the API for licensing.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
class LicenseManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`initLicense`](#initlicense) | Initializes the license for the application using the provided license key. |
| [`setDeviceFriendlyName`](#setdevicefriendlyname) | Assigns a distinctive name to the device, correlating it with its UUID. |
| [`getDeviceUUID`](#getdeviceuuid) | Returns the unique identifier of the device. |

### initLicense

Initializes the license for the application using the provided license key.

```js
static initLicense(license: string): Promise<void>
```

**Code Snippet**

```js
const License = 'DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9';
LicenseManager.initLicense(License).catch(e => {
  Alert.alert('License error', e.message);
});
```

### setDeviceFriendlyName

Assigns a distinctive name to the device, correlating it with its UUID.

```js
static setDeviceFriendlyName(name: string)
```

**Parameters**

`name`: User defined device name.

### getDeviceUUID

Returns the unique identifier of the device.

```js
static getDeviceUUID(): Promise<string>
```

**Return Value**

The device UUID.
