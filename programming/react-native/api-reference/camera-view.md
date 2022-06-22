---
layout: default-layout
title: Camera View Class - Dynamsoft Capture Vision React Native Edition
description: This page is the API reference of Camera View class
keywords: Camera view, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Camera View class
---

# DynamsoftCameraView Class

The component class of Dynamsoft Capture Vision.

## scanRegion

The property for users to specify the region of interest.

```js
scanRegion: any;
```

**Code Snippet**

```js
render() {
    let region: Region
    region = {
        regionTop: 0,
        regionLeft: 10,
        regionBottom: 55,
        regionRight: 80,
        regionMeasuredByPercentage: true
    }
    return (
        <DynamsoftCameraView
            style={{
                flex: 1,
            }}
            ref = {(ref)=>{this.scanner = ref}}
            isOverlayVisible={true}
            isScanRegionVisible={true}
            scanRegion={region}
        >
        </DynamsoftCameraView>
    );
}
```

## isScanRegionVisible

A property that indicates whether the [`scanRegion`](#scanregion) is visible.

```js
isScanRegionVisible: boolean;
```

**Code Snippet**

View code snippet in the [`scanRegion`](#scanregion) section.

## isOverlayVisible

A property that indicates whether the `overlays` are visible.

```js
isOverlayVisible: boolean;
```

**Code Snippet**

View code snippet in the [`scanRegion`](#scanregion) section.
