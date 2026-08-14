---
layout: default-layout
title: EnumLayoutElementSource - Dynamsoft Capture Vision React Native
description: Enumeration EnumLayoutElementSource of Dynamsoft Capture Vision React Native Edition defines the origin of a layout element.
keywords: layout element source
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumLayoutElementSource
---

# EnumLayoutElementSource

`EnumLayoutElementSource` describes the origin of a layout element.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumLayoutElementSource {
  LES_NONE = 0,
  LES_INPUT = 1,
  LES_INFERRED = 2
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `LES_NONE` | No element exists at this logical grid position. |
| `LES_INPUT` | Element is provided from the original input array. |
| `LES_INFERRED` | Element is reconstructed or filled in by the algorithm. |
