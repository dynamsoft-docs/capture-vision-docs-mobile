---
layout: default-layout
title: DCVCameraView Class of Dynamsoft Capture Vision Cordova Edition
description: This page is the API reference of DCVCameraView class
keywords: Camera view, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: DCVCameraView
---

# Class DCVCameraView

`DCVCameraView` is the class that used to display the view of camera and related UI elements.

```js
class DCVCameraView
```

| Property | Description |
| -------- | ----------- |
| [`bindToHtmlElement`](#bindtohtmlelement) | Bind DCVCameraView to a HTML element. |
| [`setOverlayVisible`](#overlayvisible) | A property that indicates whether the `overlays` are visible. |
| [`setTorchButton`](#torchbutton) | A property that determines whether a torch button will be displayed on the `DCVCameraView` and how the torch button will be displayed. |

## bindToHtmlElement

Bind DCVCameraView to a HTML element.

```js
bindToHtmlElement(element:HTMLElement): void;
```

**Parameters**

`element`: A HTML `<div>` for displaying `DCVCameraView`

**Code Snippet**

```js
```

## setOverlayVisible

Set whether to display highlight overlays on the detected significant areas (like barcode areas).

```js
setOverlayVisible(vis:boolean): void;
```

**Parameters**

`vis`: A boolean value that indicates whether the overlays are visible.

**Code Snippet**

```js
```

## setTorchButton

Set whether a torch button will be displayed on the `DCVCameraView` and how the torch button will be displayed.

```js
setTorchButton(btn:TorchButton): void;
```

**Parameters**

`btn`: A TorchButton object that contains torch button properties.

**Code Snippet**

```js
```
