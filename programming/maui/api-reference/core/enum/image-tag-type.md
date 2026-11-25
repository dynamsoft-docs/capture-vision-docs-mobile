---
layout: default-layout
title: EnumImageTagType - Dynamsoft Capture Vision MAUI API Reference
description: The EnumImageTagType enumeration defines the type of an image tag.
keywords: image tag type, file image, video frame, MAUI
needGenerateH3Content: true
needAutoGenerateSidebar: true
breadcrumbText: EnumImageTagType
---

# EnumImageTagType

`EnumImageTagType` specifies the type of an [`ImageTag`](../image-tag.md). Its values match the Android `EnumImageTagType` and iOS `DSImageTagType` enumerations.

**Remarks**

- Introduced in Dynamsoft Capture Vision version 3.6.5000.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
public enum EnumImageTagType
{
    ITT_FILE_IMAGE = 0,
    ITT_VIDEO_FRAME = 1
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `ITT_FILE_IMAGE` | The image is loaded from a file or a page of a PDF file. |
| `ITT_VIDEO_FRAME` | The image is captured from a video frame. |
