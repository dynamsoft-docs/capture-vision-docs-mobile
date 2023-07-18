---
layout: default-layout
Title: DSLicenseModule - Dynamsoft Core Module Android Edition API Reference
Description: The class DSLicenseModule of Dynamsoft Core Module represents the license module, which provides general functions for managing licenses.
Keywords: license module, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLicenseModule

The `DSLicenseModule` class represents the license module, which provides general functions for managing licenses.

## Definition

*Namespace*: com.dynamsoft.license
*Assembly:* DynamsoftLicense.aar

```java
class LicenseModule
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getVersion`](#getversion) | Get the version of Dynamsoft License module. |

## getVersion

Get the version of Dynamsoft License module.

```java
class func getVersion() -> String
```

**Return Value**

The version of Dynamsoft License module.

**Code Snippet**

```java
let version = LicenseModule.getVersion()
```
