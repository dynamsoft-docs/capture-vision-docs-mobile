---
layout: default-layout
title: CrossVerificationCriteria - Dynamsoft Utility Module Android Edition API Reference
description: The class CrossVerificationCriteria of Dynamsoft Utility Module defines the cross-verification criteria for multi-frame result verification.
keywords: cross-verification, criteria, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CrossVerificationCriteria

The `CrossVerificationCriteria` class defines the parameters for cross-verification of captured results across multiple frames.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class CrossVerificationCriteria
```

## Attributes

| Attribute | Type | Description |
|------- |------|-------------|
| [`frameWindow`](#framewindow) | *int* | The number of frames to consider for cross-verification. |
| [`minConsistentFrames`](#minconsistentframes) | *int* | The minimum number of frames that must contain consistent results for verification to succeed. |

### frameWindow

The number of frames to consider for cross-verification. Default value is 5 for barcode decoding.

```java
int frameWindow;
```

**Value Range**

A positive integer.

### minConsistentFrames

The minimum number of frames that must contain consistent results for verification to succeed. Default value is 2 for barcode decoding.

```java
int minConsistentFrames;
```

**Value Range**

A positive integer that should be less than or equal to `frameWindow`.
