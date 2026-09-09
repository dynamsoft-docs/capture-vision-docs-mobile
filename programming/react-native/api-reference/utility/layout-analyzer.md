---
layout: default-layout
title: LayoutAnalyzer - Dynamsoft Capture Vision React Native
description: LayoutAnalyzer class of DCV React Native provides static methods to analyze the spatial distribution of quadrilaterals.
keywords: layout analyzer, quadrilateral
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutAnalyzer

The `LayoutAnalyzer` class provides static methods to analyze the spatial distribution of quadrilaterals.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
class LayoutAnalyzer
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`analyze`](#analyze) | Analyzes the spatial distribution of quadrilaterals. |

### analyze

Analyzes the spatial distribution of quadrilaterals with optional constraints.

```js
static analyze(
    inputQuads: Quadrilateral[],
    parameter?: LayoutAnalysisParameter
): LayoutAnalysisResult
```

**Parameters**

`[in] inputQuads`: Array of input quadrilaterals.

`[in] parameter`: Optional parameters to constrain the analysis.

**Return Value**

A [`LayoutAnalysisResult`](layout-analysis-result.md) object, or null on failure.
