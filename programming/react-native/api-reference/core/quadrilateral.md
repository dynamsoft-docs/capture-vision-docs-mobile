---
layout: default-layout
title: Quadrilateral - Dynamsoft Capture Vision React Native
description: Interface Quadrilateral of DCV React Native is used to define a quadrilateral shape.
keywords: region, Quadrilateral, barcode reader, react native, capture vision
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Quadrilateral

Interface `Quadrilateral` is used to define a quadrilateral shape. This interface is mainly used by the `roi` parameter of [`SimplifiedCaptureVisionSettings`](../capture-vision-router/simplified-capture-vision-settings.md).

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface Quadrilateral
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`points`](#points) | *Array\<Point\>* | An array of four points that make up the quadrilateral. |

### points

An array of four points that make up the quadrilateral. The points list start from the top-left point of the quadrilateral and go clockwise.

```js
points: Point[];
```

**Remarks**

The coordinates are typically set in pixels. However, if you are setting a region via the [`SimplifiedCaptureVisionSettings`](../capture-vision-router/simplified-capture-vision-settings.md), you can set the coordinates of the Quadrilateral as percentages (of the frame dimensions) instead of pixels if `roiMeasuredInPercentage` is set to true.
