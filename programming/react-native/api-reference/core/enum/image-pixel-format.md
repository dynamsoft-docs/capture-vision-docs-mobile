---
layout: default-layout
title: EnumImagePixelFormat - Dynamsoft Capture Vision React Native
description: Enumeration EnumImagePixelFormat of Dynamsoft Capture Vision React Native Edition describes all supported image pixel formats.
keywords: Image pixel format
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumImagePixelFormat
---

# EnumImagePixelFormat

`EnumImagePixelFormat` is an enumeration that specifies the different pixel formats of an image. From this enumeration, you can determine if an image is binary, grayscale, or colour. 

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumPixelFormat {
  IPF_BINARY = 0,
  IPF_BINARYINVERTED = 1,
  IPF_GRAYSCALED = 2,
  IPF_NV21 = 3,
  IPF_RGB_565 = 4,
  IPF_RGB_555 = 5,
  IPF_RGB_888 = 6,
  IPF_ARGB_8888 = 7,
  IPF_RGB_161616 = 8,
  IPF_ARGB_16161616 = 9,
  IPF_ABGR_8888 = 10,
  IPF_ABGR_16161616 = 11,
  IPF_BGR_888 = 12,
  IPF_BINARY_8 = 13,
  IPF_NV12 = 14,
  IPF_BINARY_8_INVERTED = 15,
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `IPF_BINARY` | Each pixel is represented by a single bit. |
| `IPF_BINARYINVERTED` | Each pixel is represented by a single bit and the bits are inverted. |
| `IPF_GRAYSCALED` | Each pixel is represented by a single byte indicating the intensity of gray. |
| `IPF_NV21` | A YUV format with a specific arrangement of chroma and luma components. |
| `IPF_RGB_565` | Each pixel is represented by 16 bits: 5 bits for red, 6 bits for green, and 5 bits for blue. |
| `IPF_RGB_555` | Each pixel is represented by 15 bits: 5 bits each for red, green, and blue. |
| `IPF_RGB_888` | Each pixel is represented by 24 bits: 8 bits each for red, green, and blue. |
| `IPF_ARGB_8888` | Each pixel is represented by 32 bits: 8 bits each for alpha, red, green, and blue. |
| `IPF_RGB_161616` | Each pixel is represented by 48 bits: 16 bits each for red, green, and blue. |
| `IPF_ARGB_16161616` | Each pixel is represented by 64 bits: 16 bits each for alpha, red, green, and blue. |
| `IPF_ABGR_8888` | ABGR8888 pixel format, where each pixel is represented by 32 bits: 8 bits each for alpha, blue, green, and red. |
| `IPF_ABGR_16161616` | ABGR16161616 pixel format, where each pixel is represented by 64 bits: 16 bits each for alpha, blue, green, and red. |
| `IPF_BGR_888` | Each pixel is represented by 24 bits: 8 bits each for blue, green, and red. |
| `IPF_BINARY_8` | Each pixel is represented by 8 bits in a binary format. |
| `IPF_NV12` | NV12 pixel format, a YUV format with a specific arrangement of chroma and luma components. |
| `IPF_BINARY_8_INVERTED` | Inverted Binary8 pixel format, where each pixel is represented by 8 bits in a binary format and the bits are inverted. |
