---
layout: default-layout
title: CrossVerificationStatus - Dynamsoft Core Enumerations
description: The enumeration CrossVerificationStatus of Dynamsoft Core describes the status of the captured results.
keywords: cross verification status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CrossVerificationStatus
codeAutoHeight: true
---

# Enumeration CrossVerificationStatus

`CrossVerificationStatus` describes the status of the captured results.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSCrossVerificationStatus)
{
    /** The cross verification has not been performed yet. */
    DSCrossVerificationStatusNotVerified,
    /** The cross verification has been passed successfully. */
    DSCrossVerificationStatusPassed,
    /** The cross verification has failed. */
    DSCrossVerificationStatusFailed
};
```
>
```swift
public enum CrossVerificationStatus : Int
{
    /** The cross verification has not been performed yet. */
    notVerified,
    /** The cross verification has been passed successfully. */
    passed,
    /** The cross verification has failed. */
    failed
};
```
