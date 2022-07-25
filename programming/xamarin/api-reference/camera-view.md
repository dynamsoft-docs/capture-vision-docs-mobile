---
layout: default-layout
title: Camera View Class of Dynamsoft Capture Vision Xamarin Edition
description: This page is the API reference of Camera View class
keywords: Camera view, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Camera View class
---

# Class CameraView

`CameraView` is the class that used to display the view of camera and related UI elements.

```c#
class CameraView
```

| Property | Description |
| -------- | ----------- |
| [`OverlayVisible`](#overlayvisible) | A property that indicates whether the `overlays` are visible. |
| [`TorchButton`](#torchbutton) | A property that determines whether a torch button will be displayed on the `CameraView` and how the torch button will be displayed. |

## OverlayVisible

A property that indicates whether the `overlays` are visible.

```c#
bool OverlayVisible;
```

**Code Snippet**

```xml
<local:CameraView
    OverlayVisible="True"
    HorizontalOptions="FillAndExpand"
    VerticalOptions="FillAndExpand" >
```

## TorchButton

A property that determines whether a torch button will be displayed on the `CameraView` and how the torch button will be displayed.

```c#
TorchButton Torchbutton;
```

**Code Snippet**

```xml
<local:CameraView
    OverlayVisible="True"
    HorizontalOptions="FillAndExpand"
    VerticalOptions="FillAndExpand" >
    <local:CameraView.TorchButton>
        <local:TorchButton
            TorchOnImage="abc.png"
            TorchOffImage="abc.png"
            Visible="True">
            <local:TorchButton.Location>
                <local:Rect Width="50" Height="50" X="300" Y="300"></local:Rect>
            </local:TorchButton.Location>
        </local:TorchButton>
    </local:CameraView.TorchButton>
</local:CameraView>
```
