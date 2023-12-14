---
layout: default-layout
title: Utility Module Release Notes - Dynamsoft Capture Vision Android Edition
description: The release notes of DynamsoftUtility module - Dynamsoft Capture Vision Android Edition.
keywords: release notes, utility, Android
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftUtility Module

## v2.0.20

- Added a new method `SetPages` to the class `DirectoryFetcher` and class `FileFetcher`.
- The class `DirectoryFetcher` and `FileFetcher` will be able to return error codes via `ImageSourceErrorListener`
- Updated the error codes of the method `saveToFile` of the class `ImageManager`.

### Changed

- Changed the upper limit to the `DuplicateForgetTime`, which is 3 minutes.
