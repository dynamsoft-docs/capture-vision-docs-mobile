---
layout: default-layout
title: LicenseVerificationListener - Dynamsoft Capture Vision Android Edition API Reference
description: The interface LicenseVerificationListener of Dynamsoft Capture Vision Android includes methods for monitoring the license verification status.
keywords: license verification, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LicenseVerificationListener

The `LicenseVerificationListener` is a interface that includes methods for monitoring the license verification status.

## Definition

*Namespace:* com.dynamsoft.license

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
interface LicenseVerificationListener
```

| Method | Description |
| ------ | ----------- |
| [`onLicenseVerified`](#onlicenseverified) | The callback triggered when the license verification result is available. |

### onLicenseVerified

The callback triggered when the license verification result is available.

```java
void onLicenseVerified(boolean isSuccess, @Nullable Exception error);
```

**Parameters**

`[in] isSuccess`: A Boolean value indicating whether the license is verified successfully.

`[in] error`: An exception object. It carries the error code and message that describe the reason why your license activation failed.
