---
layout: default-layout
title: Core Module Release Notes - Dynamsoft Capture Vision Android Edition
description: The release notes of Dynamsoft Capture Vision Android Edition.
keywords: release notes, core, Android
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - Core Module

## 3.0.20 (10/26/2023)

### New

- Added `ImageSourceErrorListener` to receive the errors from an image source.
- Added method `setErrorListener` to class `ImageSourceAdapter` to add the `ImageSourceErrorListener`.
- Added the following error codes:
  - EC_FILE_ALREADY_EXISTS
  - EC_CREATE_FILE_FAILED
  - EC_IMGAE_DATA_INVALID

### Fixed

- Small fixes and tweaks.

### Changed

- Changed the timing of `onOriginalImageResultReceived` so that it is triggered immediately after receiving the image.

## 3.0.10 (08/10/2023)

The first version of `DynamsoftCore` Android edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
