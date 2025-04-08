---
layout: default-layout
title: Release Notes - DynamsoftCaptureVisionBundle MAUI Edition
description:  The release notes of DynamsoftCaptureVisionBundle MAUI Edition.
keywords: release notes, capture vision bundle, MAUI, dcv
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCaptureVisionRouter Module

## 2.6.1001 (03/20/2025)

### Fixed

- Fixed a bug where the `FragmentActivity` was not supported.

## 2.6.1000 (02/26/2025)

### New

- Updated the library to support .NET 9.0.

### Fixed

- Fixed a bug that could cause the build to fail when AOT compilation is enabled.
- Fixed a bug where the MRZ might not be read when using a front-facing camera of an iPad.
- Fixed a bug where the `ScanRegion` might not effect when set before `CameraView` is created.

## 2.4.2000 (10/24/2024)

The first version of Dynamsoft.CaptureVisionBundle.Maui. Supported the following features:

- [Barcode Scanning]({{ site.dbr_maui }}user-guide.html)
- [Document Scanning]({{ site.ddn_maui }}user-guide.html)
- [MRZ Scanning]({{ site.dcv_maui }}mrz.html)
