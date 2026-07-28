---
layout: default-layout
title: LayoutAnalysisParameter - Dynamsoft Capture Vision Android Edition API Reference
description: The class LayoutAnalysisParameter of Dynamsoft Capture Vision Android edition provides parameters for layout analysis.
keywords: layout analysis parameter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutAnalysisParameter

The `LayoutAnalysisParameter` class provides parameters to constrain the layout analysis.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class LayoutAnalysisParameter
```

## Attributes

| Attribute | Type | Description |
| --------- | ---- | ----------- |
| [`pattern`](#pattern) | *int* | Desired layout pattern. Use LP_UNKNOWN for auto-detection. |
| [`axes`](#axes) | *LayoutAxis[]* | Configuration for primary axis [0] and secondary axis [1]. |
| [`inputImageWidth`](#inputimagewidth) | *int* | Width of the reference image. Required when spacingUnit is MU_PERCENTAGE. |
| [`inputImageHeight`](#inputimageheight) | *int* | Height of the reference image. Required when spacingUnit is MU_PERCENTAGE. |

### pattern

Desired layout pattern. Use LP_UNKNOWN for auto-detection.

```java
@EnumLayoutPattern
int pattern;
```

### axes

Configuration for primary axis [0] and secondary axis [1].

```java
LayoutAxis[] axes;
```

### inputImageWidth

Width of the reference image. Required when spacingUnit is MU_PERCENTAGE.

```java
int inputImageWidth;
```

### inputImageHeight

Height of the reference image. Required when spacingUnit is MU_PERCENTAGE.

```java
int inputImageHeight;
```
