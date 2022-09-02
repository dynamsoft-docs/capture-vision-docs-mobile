---
layout: default-layout
title: DCVCameraView Class of Dynamsoft Capture Vision Flutter Edition
description: This page is the API reference of Camera View class
keywords: Camera view, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: DCVCameraView class
---

# DCVCameraView Class

The UI component of Dynamsoft Capture Vision. It displays the video streaming and other UI elements.

| Property | Description |
| -------- | ----------- |
| [`overlayVisible`](#overlayvisible) | A property that indicates whether the `overlays` are visible. |
| [`torchButton`](#torchbutton) | The property for users to define a torch button. |

## overlayVisible

A property that indicates whether the `overlays` are visible.

```dart
overlayVisible(bool isVisible)
```

**Code Snippet**

```dart
_cameraView.overlayVisible = true;
```

## torchButton

The property for users to define a torch button. Users can define the location, image and visibility of the button.

```dart
torchButton(TorchButton torchButton)
```
