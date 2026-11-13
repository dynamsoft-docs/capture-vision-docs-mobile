---
layout: default-layout
title: EnumImageTagType - Dynamsoft Capture Vision React Native
description: Enumeration EnumImageTagType of Dynamsoft Capture Vision React Native Edition defines the type of an image tag.
keywords: image tag type, file image, video frame
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumImageTagType
---

# EnumImageTagType

`EnumImageTagType` specifies the type of an [`ImageTag`](../image-tag.md).

**Remarks**

- Introduced in Dynamsoft Barcode Reader SDK version 11.6.5000 and Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
enum EnumImageTagType {
  ITT_FILE_IMAGE = 0,
  ITT_VIDEO_FRAME = 1
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `ITT_FILE_IMAGE` | The image is loaded from a file (or from a page of a PDF file). |
| `ITT_VIDEO_FRAME` | The image is captured from a video frame. |
