---
layout: default-layout
title: EnumLayoutPattern - Dynamsoft Capture Vision React Native
description: Enumeration EnumLayoutPattern of Dynamsoft Capture Vision React Native Edition defines the layout pattern for quadrilateral analysis.
keywords: layout pattern
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumLayoutPattern
---

# EnumLayoutPattern

`EnumLayoutPattern` describes the layout pattern for quadrilateral analysis.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumLayoutPattern {
  LP_UNKNOWN = 0,
  LP_LINES = 1,
  LP_MATRIX = 2
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `LP_UNKNOWN` | Algorithm automatically detects the best layout pattern. |
| `LP_LINES` | Elements are organized into sequential lines (rows or columns). |
| `LP_MATRIX` | Elements are organized into a strict grid/matrix structure. |
