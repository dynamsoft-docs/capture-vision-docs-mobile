---
layout: default-layout
title: ILicenseVerificationListener - Dynamsoft Capture Vision MAUI API Reference
description: The interface ILicenseVerificationListener of Dynamsoft Core Module MAUI includes methods for monitoring the license verification status.
keywords: license verification
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ILicenseVerificationListener

The `ILicenseVerificationListener` is a interface that includes methods for monitoring the license verification status.

## Definition

*Namespace:* Dynamsoft.License.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
interface ILicenseVerificationListener
```

| Method | Description |
| ------ | ----------- |
| [`OnLicenseVerified`](#onlicenseverified) | The callback triggered when the license verification result is available. |

### OnLicenseVerified

The callback triggered when the license verification result is available.

```csharp
void OnLicenseVerified(bool isSuccess, string message);
```

**Parameters**

`[in] isSuccess`: A Boolean value indicating whether the license is verified successfully.

`[in] message`: The error message that describe the reason why your license activation failed.
