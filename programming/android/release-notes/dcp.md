---
layout: default-layout
title: DCP Module Release Notes - Dynamsoft Capture Vision Android Edition
description: The release notes of DynamsoftCodeParser module - Dynamsoft Capture Vision Android Edition.
keywords: release notes, code parser, Android, DCP
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Release Notes - DynamsoftCodeParser Module

## 2.2.0 (03/07/2024)

### New

- Added the following methods to the `ParsedResult` class:
  - `retain`
  - `release`

### Break Changes

- Removed an internal logic that grouping the text line recognition result of the MRZ. The logic is replaced by the text line group definition of the parameter system.

## 2.0.20 (12/07/2023)

The first version of `DynamsoftCodeParser (DCP)` Android edition that integrate with `DynamsoftCaptureVision (DCV)` architecture.
