---
layout: default-layout
title: DCVCameraView Class of Dynamsoft Capture Vision Xamarin Edition
description: This page is the API reference of DCVCameraView class
keywords: Camera view, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: DCVCameraView
---

# Class DCVCameraView

`DCVCameraView` is the class that used to display the view of camera and related UI elements.

```c#
class DCVCameraView
```

| Property | Description |
| -------- | ----------- |
| [`OverlayVisible`](#overlayvisible) | A property that indicates whether the `overlays` are visible. |
| [`TorchButton`](#torchbutton) | A property that determines whether a torch button will be displayed on the `DCVCameraView` and how the torch button will be displayed. |

## OverlayVisible

A property that indicates whether the `overlays` are visible.

```c#
bool OverlayVisible;
```

**Code Snippet**

```xml
<local:DCVCameraView
    OverlayVisible="True"
    HorizontalOptions="FillAndExpand"
    VerticalOptions="FillAndExpand" >
```

## TorchButton

A property that determines whether a torch button will be displayed on the `DCVCameraView` and how the torch button will be displayed.

```c#
TorchButton Torchbutton;
```

**Code Snippet**

```xml
<local:DCVCameraView
    OverlayVisible="True"
    HorizontalOptions="FillAndExpand"
    VerticalOptions="FillAndExpand" >
    <local:DCVCameraView.TorchButton>
        <local:TorchButton
            TorchOnImage="abc.png"
            TorchOffImage="abc.png"
            Visible="True">
            <local:TorchButton.Location>
                <local:Rect Width="50" Height="50" X="300" Y="300"></local:Rect>
            </local:TorchButton.Location>
        </local:TorchButton>
    </local:DCVCameraView.TorchButton>
</local:DCVCameraView>
```
