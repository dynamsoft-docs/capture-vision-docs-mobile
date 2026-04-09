---
layout: default-layout
title: CrossVerificationCriteria - Dynamsoft Utility Module MAUI Edition API Reference
description: The class CrossVerificationCriteria of Dynamsoft Utility Module defines the cross-verification criteria for multi-frame result verification.
keywords: cross-verification, criteria, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CrossVerificationCriteria

The `CrossVerificationCriteria` class defines the parameters for cross-verification of captured results across multiple frames.

## Definition

*Namespace:* Dynamsoft.Utility.Maui

*Assembly:* Dynamsoft.Utility.Maui

```csharp
class CrossVerificationCriteria
```

## Properties

| Property | Type | Description |
|--------- |------|-------------|
| [`FrameWindow`](#framewindow) | *int* | The number of frames to consider for cross-verification. |
| [`MinConsistentFrames`](#minconsistentframes) | *int* | The minimum number of frames that must contain consistent results for verification to succeed. |

### frameWindow

The number of frames to consider for cross-verification. Default value is 5 for barcode decoding.

```csharp
int FrameWindow { get; set; }
```

**Value Range**

A positive integer.

### minConsistentFrames

The minimum number of frames that must contain consistent results for verification to succeed. Default value is 2 for barcode decoding.

```csharp
int MinConsistentFrames { get; set; }
```

**Value Range**

A positive integer that should be less than or equal to `frameWindow`.
