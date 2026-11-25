---
layout: default-layout
title: EnumImageTagType - Dynamsoft Capture Vision Flutter
description: Enumeration EnumImageTagType of Dynamsoft Capture Vision Flutter defines the type of an image tag.
keywords: image tag type, file image, video frame, Flutter
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumImageTagType
---

# EnumImageTagType

`EnumImageTagType` specifies the type of an [`ImageTag`](../image-tag.md). The enum indices match the native values and are sent over the platform channel as-is.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
enum EnumImageTagType {
  fileImage,
  videoFrame,
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `fileImage` | Index 0. The image is loaded from a file or a page of a PDF file. |
| `videoFrame` | Index 1. The image is captured from a video frame. |
