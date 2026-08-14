---
layout: default-layout
title: LayoutElement - Dynamsoft Capture Vision React Native
description: Interface LayoutElement of DCV React Native represents an element in a layout analysis.
keywords: layout element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutElement

The `LayoutElement` interface represents an element in a layout analysis.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface LayoutElement
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`quad`](#quad) | *Quadrilateral* | Geometric coordinates of the element. |
| [`source`](#source) | *EnumLayoutElementSource* | Origin of the element. |

### quad

Geometric coordinates of the element.

```js
quad: Quadrilateral;
```

### source

Origin of the element.

```js
source: EnumLayoutElementSource;
```
