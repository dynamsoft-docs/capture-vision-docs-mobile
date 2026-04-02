---
layout: default-layout
title: DSRect - Dynamsoft Capture Vision React Native
description: Interface DSRect of DCV React Native is used to define a rectangular region.
keywords: region, DSRect, barcode reader, react native, capture vision
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSRect

Interface `DSRect` is used to define a rectangular region.
## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface DSRect
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`left`](#left) | *number* | The left edge of the rectangle, set in pixels or as a percentage of the width of the frame. |
| [`top`](#top) | *number* | The top edge of the rectangle, set in pixels or as a percentage of the length of the frame. |
| [`right`](#right) | *number* | The right edge of the rectangle, set in pixels or as a percentage of the width of the frame. |
| [`bottom`](#bottom) | *number* | The bottom edge of the rectangle, set in pixels or as a percentage of the length of the frame. |
| [`measuredInPercentage`](#measuredinpercentage) | *number* | Determines whether the rectangle's dimensions are measured as a percentage of the total image/frame dimensions or not. |

### left

The left edge of the rectangle, set in pixels or as a percentage of the width of the frame.

```js
left: number;
```

> [!Note]
> Value range is [0.0, 1.0] when measuredInPercentage is true.

### top

The top edge of the rectangle, set in pixels or as a percentage of the length of the frame.

```js
top: number;
```

> [!Note]
> Value range is [0.0, 1.0] when measuredInPercentage is true.

### right

The right edge of the rectangle, set in pixels or as a percentage of the width of the frame.

```js
right: number;
```

> [!Note]
> Value range is [0.0, 1.0] when measuredInPercentage is true.

### bottom

The bottom edge of the rectangle, set in pixels or as a percentage of the length of the frame.

```js
bottom: number;
```

> [!Note]
> Value range is [0.0, 1.0] when measuredInPercentage is true.

### measuredInPercentage

Determines whether the rectangle's dimensions are measured as a percentage of the total image/frame dimensions or not.

```js
measuredInPercentage: number | boolean;
```
