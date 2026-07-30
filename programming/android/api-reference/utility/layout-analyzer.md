---
layout: default-layout
title: LayoutAnalyzer - Dynamsoft Capture Vision Android Edition API Reference
description: The class LayoutAnalyzer of Dynamsoft Capture Vision Android edition provides quadrilateral layout analysis functionality.
keywords: layout analyzer, quadrilateral, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutAnalyzer

The `LayoutAnalyzer` class provides static methods to analyze the spatial distribution of quadrilaterals.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class LayoutAnalyzer
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`analyze(inputQuads)`](#analyzeinputquads) | Analyzes the spatial distribution of quadrilaterals. |
| [`analyze(inputQuads,parameter)`](#analyzeinputquadsparameter) | Analyzes the spatial distribution of quadrilaterals with optional constraints. |

### analyze(inputQuads)

Analyzes the spatial distribution of quadrilaterals.

```java
static LayoutAnalysisResult analyze(Quadrilateral[] inputQuads);
```

**Parameters**

`[in] inputQuads`: Array of input quadrilaterals.

**Return Value**

A [`LayoutAnalysisResult`](layout-analysis-result.md) object, or null on failure.

### analyze(inputQuads,parameter)

Analyzes the spatial distribution of quadrilaterals with optional constraints.

```java
static LayoutAnalysisResult analyze(Quadrilateral[] inputQuads, LayoutAnalysisParameter parameter);
```

**Parameters**

`[in] inputQuads`: Array of input quadrilaterals.

`[in] parameter`: Optional parameters to constrain the analysis.

**Return Value**

A [`LayoutAnalysisResult`](layout-analysis-result.md) object, or null on failure.
