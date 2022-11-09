---
layout: default-layout
title: Interface IDCVCameraEnhancer of Dynamsoft Capture Vision Xamarin Edition
description: This page is the API reference of Interface IDCVCameraEnhancer
keywords: Interface IDCVCameraEnhancer, API Reference, Xamarin, Xamarin Forms
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: IDCVCameraEnhancer
---

# Interface IDCVCameraEnhancer

The interface `IDCVCameraEnhancer` provides camera and related hardware controlling APIs.

```c#
interface IDCVCameraEnhancer
```

<style>
  .markdown-body > table {
    display: table;
    width: 100%;
  }
  .markdown-body > table tr th:first-child {
    width: 30%;
  }
</style>

| Method | Description |
| ------- | ----------- |
| [`ScanRegion`](#scanregion) | The property for users to specify the region of interest. |
| [`Open`](#open) | Open the camera. |
| [`Close`](#close) | Close the camera. |
| [`TurnOnTorch`](#turnontorch) | Turn on the torch. |
| [`TurnOffTorch`](#turnofftorch) | Turn off the torch. |

## ScanRegion

Specify a region of interest.

```c#
Region ScanRegion { get; set; }
```

**Parameters**

`scanRegion`: An object of [`Region`](class-region.md) class which indicates the location of the region.

**Code Snippet**

```c#
DCVXamarin.Region scanRegion = new DCVXamarin.Region();
scanRegion.RegionTop = 30;
scanRegion.RegionBottom = 70;
scanRegion.RegionLeft = 15;
scanRegion.RegionRight = 85;
scanRegion.RegionMeasuredByPercentage = 1;
camera.ScanRegion = scanRegion;
```

**Related APIs**

- [Region](class-region.md)

## Open

Open the camera.

```c#
void Open();
```

## Close

Close the camera.

```c#
void Close();
```

## TurnOnTorch

Turn on the torch.

```c#
void TurnOnTorch();
```

## TurnOffTorch

Turn off the torch.

```c#
void TurnOffTorch();
```
