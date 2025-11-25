---
layout: default-layout
title: Quadrilateral Class - Dynamsoft Capture Vision Flutter
description: Quadrilateral class of DCV Flutter is used to define a quadrilateral shape.
keywords: region, Quadrilateral, barcode reader, flutter, capture vision
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Quadrilateral

The `Quadrilateral` class is used to define a quadrilateral shape. This class is mainly used by the `roi` parameter of [`SimplifiedCaptureVisionSettings`](simplified-capture-vision-settings.md).

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class Quadrilateral
```

## Constructors

```dart
Quadrilateral({required this.points});
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`points`](#points) | *List\<Point\>* | A list of four points that make up the quadrilateral. |

### points

A list of four points that make up the quadrilateral. The points list start from the top-left point of the quadrilateral and go clockwise.

```dart
List<Point<int>> points;
```

**Remarks**

The coordinates are typically set in pixels. However, if you are setting a region via the [`SimplifiedCaptureVisionSettings`](../capture-vision-router/simplified-capture-vision-settings.md), you can set the coordinates of the Quadrilateral as percentages (of the frame dimensions) instead of pixels if `roiMeasuredInPercentage` is set to true.
