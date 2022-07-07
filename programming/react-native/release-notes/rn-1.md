---
layout: default-layout
title: Release Notes - React Native - Dynamsoft Capture Vision
description: This is the release notes of Dynamsoft Capture Vision - React Native Edition.
keywords:  Capture Vision, React Native, Release Notes
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: 1.x
---

# Release Notes for React Native SDK - 1.x

## 1.1.1 (07/06/2022)

### Fixed

- Fixed a bug that might cause a crash when using the library in React Native 0.69.0+.
- Fixed a bug that [`torchState`](../api-reference/camera-view.md#torchstate) might not be set correctly.

## 1.1.0 (07/01/2022)

### Highlights

{%- include release-notes/product-highlight-1.1.0.md -%}

### Changelog

#### New

- Added a new property [`torchState`](../api-reference/camera-view.md#torchstate) and a new enumeration [`EnumTorchState`](../api-reference/enum-torch-state.md). User can turn on/off the torchlight by changing the value of [`torchState`](../api-reference/camera-view.md#torchstate).
- Added a new property [`torchButton`](../api-reference/camera-view.md#torchbutton) and two new interfaces, [`TorchButton`](../api-reference/interface-torch-button.md) and [`Rect`](../api-reference/interface-rect.md), for users to configure the torch button on the UI.

## 1.0.0 (06/23/2022)

### Highlights

{%- include release-notes/product-highlight-1.0.0.md -%}
