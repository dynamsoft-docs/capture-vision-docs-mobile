---
layout: default-layout
title: CrossVerificationCriteria - Dynamsoft Capture Vision Flutter Edition API Reference
description: The class CrossVerificationCriteria of Dynamsoft Capture Vision Flutter defines the cross-verification criteria for multi-frame result verification.
keywords: cross-verification, criteria, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CrossVerificationCriteria

The `CrossVerificationCriteria` class defines the parameters for cross-verification of captured results across multiple frames.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class CrossVerificationCriteria
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`frameWindow`](#framewindow) | *int* | The number of frames to consider for cross-verification. |
| [`minConsistentFrames`](#minconsistentframes) | *int* | The minimum number of frames that must contain consistent results for verification to succeed. |

### frameWindow

The number of frames to consider for cross-verification. Default value is 5 for barcode decoding.

```dart
int frameWindow;
```

**Value Range**

A positive integer.

### minConsistentFrames

The minimum number of frames that must contain consistent results for verification to succeed. Default value is 2 for barcode decoding.

```dart
int minConsistentFrames;
```

**Value Range**

A positive integer that should be less than or equal to `frameWindow`.
