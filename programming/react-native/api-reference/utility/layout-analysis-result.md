---
layout: default-layout
title: LayoutAnalysisResult - Dynamsoft Capture Vision React Native
description: Interface LayoutAnalysisResult of DCV React Native represents the comprehensive results of the layout analysis.
keywords: layout analysis result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutAnalysisResult

The `LayoutAnalysisResult` interface represents the comprehensive results of the layout analysis.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface LayoutAnalysisResult
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`inferredQuads`](#inferredquads) | *Quadrilateral[]* | Array of newly generated quadrilaterals. |
| [`elements`](#elements) | *LayoutElement[][]* | A 2D array of layout elements [rowCount][colCount]. |
| [`rowCount`](#rowcount) | *number* | Number of rows in the analyzed layout. |
| [`colCount`](#colcount) | *number* | Maximum number of columns across all rows. |
| [`detectedPattern`](#detectedpattern) | *EnumLayoutPattern* | The actual layout pattern identified by the engine. |
| [`errorCode`](#errorcode) | *number* | 0 for success, non-zero for error. |

### inferredQuads

Array of newly generated quadrilaterals.

```js
inferredQuads: Quadrilateral[];
```

### elements

A 2D array of layout elements [rowCount][colCount].

```js
elements: LayoutElement[][];
```

### rowCount

Number of rows in the analyzed layout.

```js
rowCount: number;
```

### colCount

Maximum number of columns across all rows.

```js
colCount: number;
```

### detectedPattern

The actual layout pattern identified by the engine.

```js
detectedPattern: EnumLayoutPattern;
```

### errorCode

0 for success, non-zero for error.

```js
errorCode: number;
```
