---
layout: default-layout
title: EnumVideoFrameQuality - Dynamsoft Capture Vision MAUI API Reference
description: The EnumVideoFrameQuality enumeration defines the quality of a video frame.
keywords: video frame quality, frame filter, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
breadcrumbText: EnumVideoFrameQuality
---

# EnumVideoFrameQuality

`EnumVideoFrameQuality` specifies the quality of a video frame. Its values match the Android `EnumVideoFrameQuality` and iOS `DSFrameQuality` enumerations.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
public enum EnumVideoFrameQuality
{
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
