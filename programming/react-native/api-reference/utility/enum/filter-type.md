---
layout: default-layout
title: EnumFilterType - Dynamsoft Capture Vision React Native
description: Enumeration EnumFilterType of Dynamsoft Capture Vision React Native Edition defines the types of filters that can be applied to an image.
keywords: filter type, capture vision, image, processor
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumFilterType
---

# EnumFilterType

`EnumFilterType` is an enumeration that specifies the different types of filters that can be applied to an image for further processing.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumFilterType {
  FT_HIGH_PASS = 0,
  FT_SHARPEN = 1,
  FT_SMOOTH = 2
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `FT_HIGH_PASS` | Enhances the edges and fine details by attenuating low-frequency components. |
| `FT_SHARPEN` | Increases contrast along edges to make the image appear more defined. |
| `FT_SMOOTH` | Reduces noise and detail by averaging pixel values, creating a softening effect. |
