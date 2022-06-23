---
layout: default-layout
title: Camera View Class of Dynamsoft Capture Vision Flutter Edition
description: This page is the API reference of Camera View class
keywords: Camera view, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Camera View class
---

# DynamsoftCameraView Class

The UI component of Dynamsoft Capture Vision. It provides the following functions:

- Implement basic camera control like open, close, etc.
- Define the scan area where barcode reading is performed.
- Display the video preview, overlay, scan region etc.

| Property | Description |
| ------- | ----------- |
| [`scanRegion`](#scanregion) | The property for users to specify the region of interest. |
| [`scanRegionVisible`](#scanregionvisible) | A property that indicates whether the [`scanRegion`](#scanregion) is visible. |
| [`overlayVisible`](#overlayvisible) | A property that indicates whether the `overlays` are visible. |

## scanRegion

The property for users to specify the region of interest.

```dart
scanRegion(Region? region)
```

**Code Snippet**

```dart
final DynamsoftCameraView _cameraView = DynamsoftCameraView();
Region scanRegion = Region(regionTop: 20, regionBottom: 80, regionLeft: 20, regionRight: 80, regionMeasuredByPercentage: true);
_cameraView.scanRegion = scanRegion;
```

## scanRegionVisible

A property that indicates whether the [`scanRegion`](#scanregion) is visible.

```dart
scanRegionVisible(bool isVisible)
```

**Code Snippet**

```dart
_cameraView.scanRegionVisible = true;
```

## overlayVisible

A property that indicates whether the `overlays` are visible.

```dart
overlayVisible(bool isVisible)
```

**Code Snippet**

```dart
_cameraView.overlayVisible = true;
```
