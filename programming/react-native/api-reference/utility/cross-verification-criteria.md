---
layout: default-layout
title: CrossVerificationCriteria - Dynamsoft Capture Vision React Native Edition API Reference
description: The interface CrossVerificationCriteria of Dynamsoft Capture Vision React Native defines the cross-verification criteria for multi-frame result verification.
keywords: cross-verification, criteria, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CrossVerificationCriteria

The `CrossVerificationCriteria` class defines the parameters for cross-verification of captured results across multiple frames.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```tsx
export interface CrossVerificationCriteria
```

## Attributes

| Attribute | Type | Description |
|------- |------|-------------|
| [`frameWindow`](#framewindow) | *number* | The number of frames to consider for cross-verification. |
| [`minConsistentFrames`](#minconsistentframes) | *number* | The minimum number of frames that must contain consistent results for verification to succeed. |

### frameWindow

The number of frames to consider for cross-verification. Default value is 5 for barcode decoding.

```tsx
frameWindow: number;
```

**Value Range**

A positive integer.

### minConsistentFrames

The minimum number of frames that must contain consistent results for verification to succeed. Default value is 2 for barcode decoding.

```tsx
minConsistentFrames: number;
```

**Value Range**

A positive integer that should be less than or equal to `frameWindow`.
