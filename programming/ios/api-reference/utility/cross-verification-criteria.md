---
layout: default-layout
title: DSCrossVerificationCriteria - Dynamsoft Utility Module iOS Edition API Reference
description: The class DSCrossVerificationCriteria of Dynamsoft Utility Module defines the cross-verification criteria for multi-frame result verification.
keywords: cross-verification, criteria, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSCrossVerificationCriteria

The `DSCrossVerificationCriteria` class defines the parameters for cross-verification of captured results across multiple frames.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCrossVerificationCriteria : NSObject
```
2. 
```swift
class CrossVerificationCriteria : NSObject
```

## Attributes

| Attribute | Type | Description |
|------- |------|-------------|
| [`frameWindow`](#framewindow) | *NSInteger* | The number of frames to consider for cross-verification. |
| [`minConsistentFrames`](#minconsistentframes) | *NSInteger* | The minimum number of frames that must contain consistent results for verification to succeed. |

### frameWindow

The number of frames to consider for cross-verification. Default value is 5 for barcode decoding.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger frameWindow;
```
2. 
```swift
var frameWindow: Int { get set }
```

**Value Range**

A positive integer.

### minConsistentFrames

The minimum number of frames that must contain consistent results for verification to succeed. Default value is 2 for barcode decoding.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger minConsistentFrames;
```
2. 
```swift
var minConsistentFrames: Int { get set }
```

**Value Range**

A positive integer that should be less than or equal to `frameWindow`.
