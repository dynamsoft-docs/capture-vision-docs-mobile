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

The component class of Dynamsoft Capture Vision.

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

## isScanRegionVisible

A property that indicates whether the [`scanRegion`](#scanregion) is visible.

```dart
isScanRegionVisible(bool isVisible)
```

**Code Snippet**

```dart
_cameraView.isScanRegionVisible = true;
``
## isOverlayVisible

A property that indicates whether the `overlays` are visible.

```dart
isOverlayVisible(bool isVisible)
```

**Code Snippet**

```dart
_cameraView.isOverlayVisible = true;
```
