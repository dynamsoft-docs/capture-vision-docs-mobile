---
layout: default-layout
title: DCE Module Release Notes - Dynamsoft Capture Vision Android Edition
description: The release notes of DynamsoftCameraEnhancer module - Dynamsoft Capture Vision Android Edition.
keywords: release notes, camera enhancer, Android, DCE
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCameraEnhancer Module

## 4.2.10 (05/15/2024)

- Small fixes and tweaks.

## 4.2.0 (03/07/2024)

Internal changes to be compatible with DynamsoftCaptureVisionRouter v2.2.10.

## 4.0.2 (12/07/2023)

- Fixed a bug where method `getSelectedDrawingItem` might not return correctly.

## 4.0.1 (10/26/2023)

- Added a new method `setDrawingItemClickListener` to class `CameraView` & `ImageEditorView`. You can set a `DrawingItemClickListener` to the view to monitor the click events of the `DrawingItems`.
- Fixed a bug where `getDrawingItems` returns the previous coordinate information when `DrawingItems` are edited on the ImageEditorView.
- Applied some internal changes to the resolution control and scan region UI setting APIs.

## 4.0.0 (08/10/2023)

- Refactored the camera-controlling APIs of the `CameraEnhancer` class.
- Refactored the UI configuration APIs.
- Updated the scan region setting APIs. Support scan laser setting.
- Added new features to set the coordinate base of the `DrawingItems` and tip messages.
- Other minor changes on the API names and behaviors.
- Added tip configuration APIs to display tip messages.
- A new class Note has been added to enable `DrawingItems` to carry additional information.
