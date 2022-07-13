---
layout: default-layout
title: Interface ICameraEnhancer of Dynamsoft Capture Vision Xamarin Edition
description: This page is the API reference of Interface ICameraEnhancer
keywords: Interface ICameraEnhancer, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: ICameraEnhancer
---

# Interface ICameraEnhancer

The interface `ICameraEnhancer` provides camera and camera related hardware controlling APIs.

```c#
interface ICameraEnhancer
```

| Method | Description |
| ------- | ----------- |
| [`SetScanRegion`](#setscanregion) | The property for users to specify the region of interest. |
| [`Open`](#open) | Open the camera. |
| [`Close`](#close) | Close the camera. |
| [`TurnOnTorch`](#turnontorch) | Turn on the torch. |
| [`TurnOffTorch`](#turnofftorch) | Turn off the torch. |

| Property | Description |
| -------- | ----------- |
| [`ScanRegionVisible`](#scanregionvisible) | A property that indicates whether the `ScanRegion` is visible. |

## Method Detail

### SetScanRegion

Specify a region of interest.

```c#
void SetScanRegion(Region scanRegion);
```

**Parameters**

`scanRegion`: An object of `Region` class. It contains the properitirs that indicates the location of the region. View more in [`Region`](class-region.md).

**Code Snippet**

```c#
DCVXamarin.Region scanRegion = new DCVXamarin.Region();
scanRegion.RegionTop = 30;
scanRegion.RegionBottom = 70;
scanRegion.RegionLeft = 15;
scanRegion.RegionRight = 85;
scanRegion.RegionMeasuredByPercentage = 1;
App.camera.SetScanRegion(scanRegion);
```

**Related APIs**

- [Region](class-region.md)

### Open

Open the camera.

```c#
void Open();
```

### Close

Close the camera.

```c#
void Close();
```

### TurnOnTorch

Turn on the torch.

```c#
void TurnOnTorch();
```

### TurnOffTorch

Turn off the torch.

```c#
void TurnOffTorch();
```

## Property Detail

### ScanRegionVisible

A property that indicates whether the [`ScanRegion`](#scanregion) is visible.

```c#
bool ScanRegionVisible;
```
