---
layout: default-layout
title: DSLicenseVerificationListener - Dynamsoft Core Module iOS Edition API Reference
description: The protocol DSLicenseVerificationListener of Dynamsoft Core Module includes methods for monitoring the license verification status.
keywords: license verification, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLicenseVerificationListener

The `DSLicenseVerificationListener` is a protocol that includes methods for monitoring the license verification status.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@protocol DSLicenseVerificationListener <NSObject>
```
2. 
```swift
protocol LicenseVerificationListener : NSObjectProtocol
```

| Method | Description |
| ------ | ----------- |
| [`onLicenseVerified`](#onlicenseverified) | The callback triggered when the license verification result is available. |

### onLicenseVerified

The callback triggered when the license verification result is available.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onLicenseVerified:(BOOL)isSuccess error:(NSError * _Nullable)error;
```
2. 
```swift
func onLicenseVerified(_ isSuccess: Bool, error: Error?)
```

**Parameters**

`isSuccess`: A Boolean value indicating whether the license is verified successfully.

`error`: An `NSError` pointer. If an error occurs, it will represent the error information.
