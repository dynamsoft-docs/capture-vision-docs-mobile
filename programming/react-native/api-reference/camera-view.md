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

The UI component of Dynamsoft Capture Vision. It provides the following functions:

- Implement basic camera control like open, close, etc.
- Define the scan area where barcode reading is performed.
- Display the video preview, overlay, scan region etc.

| Property | Description |
| ------- | ----------- |
| [`scanRegion`](#scanregion) | The property for users to specify the region of interest. |
| [`scanRegionVisible`](#scanregionvisible) | A property that indicates whether the [`scanRegion`](#scanregion) is visible. |
| [`overlayVisible`](#overlayvisible) | A property that indicates whether the `overlays` are visible. |

## scanRegion

The property for users to specify the region of interest.

```js
scanRegion: Region;
```

**Code Snippet**

```jsx
render() {
    let region = {
        regionTop: 0,
        regionLeft: 10,
        regionBottom: 55,
        regionRight: 80,
        regionMeasuredByPercentage: true
    }
    return (
        <DynamsoftCameraView
            style={{
                flex: 1
            }}
            ref = {(ref)=>{this.scanner = ref}}
            overlayVisible={true}
            scanRegionVisible={true}
            scanRegion={region}
        >
        </DynamsoftCameraView>
    );
}
```

## scanRegionVisible

A property that indicates whether the [`scanRegion`](#scanregion) is visible.

```js
scanRegionVisible: boolean;
```

**Code Snippet**

View code snippet in the [`scanRegion`](#scanregion) section.

## overlayVisible

A property that indicates whether the `overlays` are visible.

```js
overlayVisible: boolean;
```

**Code Snippet**

View code snippet in the [`scanRegion`](#scanregion) section.
