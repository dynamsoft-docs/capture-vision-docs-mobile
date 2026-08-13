---
layout: default-layout
title: EnumMeasureUnit - Dynamsoft Capture Vision React Native
description: Enumeration EnumMeasureUnit of Dynamsoft Capture Vision React Native Edition defines the unit of measurement for a value.
keywords: measure unit, pixel, percentage
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumMeasureUnit
---

# EnumMeasureUnit

`EnumMeasureUnit` specifies how a numeric value should be interpreted relative to a reference dimension.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumMeasureUnit {
  MU_PIXEL = 0,
  MU_PERCENTAGE = 1
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `MU_PIXEL` | The value is an absolute pixel count. |
| `MU_PERCENTAGE` | The value is a percentage of the reference dimension (e.g. 25 = 25%). |
