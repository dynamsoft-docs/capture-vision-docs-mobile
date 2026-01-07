---
layout: default-layout
title: EnumColourChannelUsageType - Dynamsoft Capture Vision React Native Enumerations
description: Enumeration EnumColourChannelUsageType of Dynamsoft Capture Vision React Native Edition defines the available colour channels for the image source to use when capturing images or frames
keywords: colour channel, capture vision, camera, enhancer, pixel, format
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumColourChannelUsageType
---

# EnumColourChannelUsageType

`EnumColourChannelUsageType` is an enumeration that specifies the different colour channels that are available to the Camera Enhancer. The colour channel affects the pixel type that the captured images or frames will come out in, so it can output grayscale or colour images.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumColourChannelUsageType {
  CCUT_AUTO = 0,
  CCUT_FULL_CHANNEL = 1,
  CCUT_Y_CHANNEL_ONLY = 2,
  CCUT_RGB_R_CHANNEL_ONLY = 3,
  CCUT_RGB_G_CHANNEL_ONLY = 4,
  CCUT_RGB_B_CHANNEL_ONLY = 5
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `CCUT_AUTO` | Automatic colour channel usage determination based on image pixel format and scene. |
| `CCUT_FULL_CHANNEL` | Uses all colour channels to output a full colour image. |
| `CCUT_Y_CHANNEL_ONLY` | Uses only the luminance channel to output a grayscale image. |
| `CCUT_RGB_R_CHANNEL_ONLY` | Uses only the red channel of the RGB space. |
| `CCUT_RGB_G_CHANNEL_ONLY` | Uses only the green channel of the RGB space. |
| `CCUT_RGB_B_CHANNEL_ONLY` | Uses only the blue channel of the RGB space. |
