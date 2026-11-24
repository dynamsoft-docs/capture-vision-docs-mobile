---
layout: default-layout
title: EnumVideoFrameQuality - Dynamsoft Capture Vision Flutter
description: Enumeration EnumVideoFrameQuality of Dynamsoft Capture Vision Flutter defines the quality of a video frame.
keywords: video frame quality, frame filter, Flutter
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumVideoFrameQuality
---

# EnumVideoFrameQuality

`EnumVideoFrameQuality` specifies the quality of a video frame. The enum indices match the native values.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
enum EnumVideoFrameQuality {
  high,
  low,
  unknown,
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `high` | Index 0. The frame quality is recognized to be high. |
| `low` | Index 1. The frame quality is recognized to be low. |
| `unknown` | Index 2. The frame filter is not enabled, so the frame quality is unknown. |
