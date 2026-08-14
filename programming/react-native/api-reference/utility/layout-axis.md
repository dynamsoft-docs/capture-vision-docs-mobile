---
layout: default-layout
title: LayoutAxis - Dynamsoft Capture Vision React Native
description: Interface LayoutAxis of DCV React Native provides axis configuration for layout analysis.
keywords: layout axis
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# LayoutAxis

The `LayoutAxis` interface provides configuration for a single axis in layout analysis.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface LayoutAxis
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`elementCount`](#elementcount) | *number* | Expected number of elements along this axis. Use -1 for auto-detection. |
| [`isStaggered`](#isstaggered) | *boolean* | Whether the layout uses an offset/staggered pattern. |
| [`angle`](#angle) | *number* | Target angle [0, 180]. Use -1 for auto-detection. |
| [`isEqualSpacing`](#isequalspacing) | *boolean* | Force equal gaps between elements. When false, spacing is ignored. |
| [`spacing`](#spacing) | *number* | Spacing between elements along this axis. Use -1 for auto-detection. |
| [`spacingUnit`](#spacingunit) | *EnumMeasureUnit* | Interpretation mode for the spacing value. |

### elementCount

Expected number of elements along this axis. Use -1 for auto-detection.

```js
elementCount: number;
```

### isStaggered

Whether the layout uses an offset/staggered pattern.

```js
isStaggered: boolean;
```

### angle

Target angle [0, 180]. Use -1 for auto-detection.

```js
angle: number;
```

### isEqualSpacing

Force equal gaps between elements. When false, spacing is ignored.

```js
isEqualSpacing: boolean;
```

### spacing

Spacing between elements along this axis. Use -1 for auto-detection.

```js
spacing: number;
```

### spacingUnit

Interpretation mode for the spacing value.

```js
spacingUnit: EnumMeasureUnit;
```
