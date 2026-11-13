---
layout: default-layout
title: EnumVideoFrameQuality - Dynamsoft Capture Vision React Native
description: Enumeration EnumVideoFrameQuality of Dynamsoft Capture Vision React Native Edition defines the quality of a video frame.
keywords: video frame quality, frame filter
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumVideoFrameQuality
---

# EnumVideoFrameQuality

`EnumVideoFrameQuality` specifies the quality of a video frame.

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.6.5000 and Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumVideoFrameQuality {
  VFQ_HIGH = 0,
  VFQ_LOW = 1,
  VFQ_UNKNOWN = 2
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `VFQ_HIGH` | The frame quality is recognized to be high. |
| `VFQ_LOW` | The frame quality is recognized to be low. |
| `VFQ_UNKNOWN` | The frame filter is not enabled, so the frame quality is unknown. |
