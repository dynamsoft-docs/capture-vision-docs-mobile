---
layout: default-layout
title: EnumGrayscaleTransformationMode - Dynamsoft Capture Vision React Native
description: Enumeration EnumGrayscaleTransformationMode of Dynamsoft Capture Vision React Native Edition describes all available grayscale transformation modes.
keywords: Grayscale transformation modes
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumGrayscaleTransformationMode
---

# EnumGrayscaleTransformationMode

`EnumGrayscaleTransformationMode` is an enumeration that determines which grayscale enhancement modes the library will apply before the detection process to improve the read rate of the barcodes in a given image or frame.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumGrayscaleTransformationMode {
  GTM_SKIP = 0x0,
  GTM_INVERTED = 0x1,
  GTM_ORIGINAL = 0x2,
  GTM_AUTO = 0x4
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `GTM_SKIP` | Bypasses grayscale transformation, leaving the image in its current state without any modification to its grayscale values. This mode is selected when no alteration of the grayscale data is desired, passing the image through to subsequent operations without modification. |
| `GTM_INVERTED` | Applies an inversion to the grayscale values of the image, effectively transforming light elements to dark and vice versa. This mode is particularly useful for images with light text on dark backgrounds, enhancing visibility for further processing. |
| `GTM_ORIGINAL` | Maintains the original grayscale values of the image without any transformation. This mode is suited for images with dark elements on light backgrounds, ensuring the natural contrast and detail are preserved for subsequent analysis. |
| `GTM_AUTO` | Delegates the choice of grayscale transformation to the library's algorithm, which automatically determines the most suitable transformation based on the image's characteristics. This mode is beneficial when the optimal transformation is not known in advance or varies across different images. |
