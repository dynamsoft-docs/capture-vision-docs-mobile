---
layout: default-layout
Title: DSLicenseVerificationListener - Dynamsoft Core Module Android Edition API Reference
Description: The protocol DSLicenseVerificationListener of Dynamsoft Core Module includes methods for monitoring the license verification status.
Keywords: license verification, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLicenseVerificationListener

The `DSLicenseVerificationListener` is a protocol that includes methods for monitoring the license verification status.

## Definition

*Namespace*: com.dynamsoft.license
*Assembly:* DynamsoftLicense.aar

```java
interface LicenseVerificationListener
```

### onLicenseVerified

The method that is triggered when the license server returns the verification info.

```java
func onLicenseVerified(_ isSuccess: Bool, error: Error?)
```

**Parameters**

`isSuccess`: A Boolean value indicating whether the license is verified successfully.  
`error`: An NSError pointer. It carries the error code and message that describe the reason why your license activation failed.
