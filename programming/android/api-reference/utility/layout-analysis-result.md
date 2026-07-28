---
layout: default-layout
title: LayoutAnalysisResult - Dynamsoft Capture Vision Android Edition API Reference
description: The class LayoutAnalysisResult of Dynamsoft Capture Vision Android edition represents the results of a layout analysis.
keywords: layout analysis result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutAnalysisResult

The `LayoutAnalysisResult` class represents the comprehensive results of the layout analysis.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class LayoutAnalysisResult
```

## Attributes

| Attribute | Type | Description |
| --------- | ---- | ----------- |
| [`inferredQuads`](#inferredquads) | *Quadrilateral[]* | Array of newly generated quadrilaterals. |
| [`elements`](#elements) | *LayoutElement[][]* | A 2D array of layout elements [rowCount][colCount]. |
| [`rowCount`](#rowcount) | *int* | Number of rows in the analyzed layout. |
| [`colCount`](#colcount) | *int* | Maximum number of columns across all rows. |
| [`detectedPattern`](#detectedpattern) | *int* | The actual layout pattern identified by the engine. |
| [`errorCode`](#errorcode) | *int* | 0 for success, non-zero for error. |

### inferredQuads

Array of newly generated quadrilaterals.

```java
Quadrilateral[] inferredQuads;
```

### elements

A 2D array of layout elements [rowCount][colCount].

```java
LayoutElement[][] elements;
```

### rowCount

Number of rows in the analyzed layout.

```java
int rowCount;
```

### colCount

Maximum number of columns across all rows.

```java
int colCount;
```

### detectedPattern

The actual layout pattern identified by the engine.

```java
@EnumLayoutPattern
int detectedPattern;
```

### errorCode

0 for success, non-zero for error.

```java
int errorCode;
```
