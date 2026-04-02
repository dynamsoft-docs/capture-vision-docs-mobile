---
layout: default-layout
title: DSRect Class - Dynamsoft Capture Vision Flutter
description: DSRect class of DCV Flutter is used to define a rectangular region.
keywords: region, DSRect, barcode reader, flutter, capture vision
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSRect

The `DSRect` class is used to define a rectangular region. This is typically used by the `CameraEnhancer` class to set a scan region.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class DSRect
```

## Properties

### left

The left edge of the rectangle, set in pixels or as a percentage of the width of the frame.

```dart
double left;
```

> [!Note]
> The valid range is [0.0, 1.0] when measuredInPercentage is true.

### top

The top edge of the rectangle, set in pixels or as a percentage of the length of the frame.

```dart
double top;
```

> [!Note]
> The valid range is [0.0, 1.0] when measuredInPercentage is true.

### right

The right edge of the rectangle, set in pixels or as a percentage of the width of the frame.

```dart
double right;
```

> [!Note]
> The valid range is [0.0, 1.0] when measuredInPercentage is true.

### bottom

The bottom edge of the rectangle, set in pixels or as a percentage of the length of the frame.

```dart
double bottom;
```

> [!Note]
> The valid range is [0.0, 1.0] when measuredInPercentage is true.

### measuredInPercentage

Determines whether the rectangle's dimensions are measured as a percentage of the total image/frame dimensions or not.

```dart
bool measuredInPercentage;
```

## Code Snippet

```dart
final scanRegion = DSRect(left: 0.15, top: 0.3, right: 0.85, bottom: 0.7, measuredInPercentage: true);
await _camera.setScanRegion(scanRegion);
```