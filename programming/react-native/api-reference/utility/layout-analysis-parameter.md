---
layout: default-layout
title: LayoutAnalysisParameter - Dynamsoft Capture Vision React Native
description: Interface LayoutAnalysisParameter of DCV React Native provides parameters for layout analysis.
keywords: layout analysis parameter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutAnalysisParameter

The `LayoutAnalysisParameter` interface provides parameters to constrain the layout analysis.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface LayoutAnalysisParameter
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`pattern`](#pattern) | *EnumLayoutPattern* | Desired layout pattern. Use LP_UNKNOWN for auto-detection. |
| [`axes`](#axes) | *LayoutAxis[]* | Configuration for primary axis [0] and secondary axis [1]. |
| [`inputImageWidth`](#inputimagewidth) | *number* | Width of the reference image. Required when spacingUnit is MU_PERCENTAGE. |
| [`inputImageHeight`](#inputimageheight) | *number* | Height of the reference image. Required when spacingUnit is MU_PERCENTAGE. |

### pattern

Desired layout pattern. Use LP_UNKNOWN for auto-detection.

```js
pattern: EnumLayoutPattern;
```

### axes

Configuration for primary axis [0] and secondary axis [1].

```js
axes: LayoutAxis[];
```

### inputImageWidth

Width of the reference image. Required when spacingUnit is MU_PERCENTAGE.

```js
inputImageWidth: number;
```

### inputImageHeight

Height of the reference image. Required when spacingUnit is MU_PERCENTAGE.

```js
inputImageHeight: number;
```
