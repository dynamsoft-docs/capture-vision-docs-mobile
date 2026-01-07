---
layout: default-layout
title: EnumColourChannelUsageType - Dynamsoft Vision Router MAUI Enumerations
description: The enumeration ColourChannelUsageType of Dynamsoft Vision Router describes the type of CapturedResultItem.
keywords: capture result item type, multi-frame cross filter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ColourChannelUsageType
---

# Enumeration ColourChannelUsageType

`ColourChannelUsageType` describes the type of `CapturedResultItem`.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
public enum EnumColourChannelUsageType
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
    CCUT_AUTO = 0,
    /** Use all available color channels for processing. */
    CCUT_FULL_CHANNEL = 1,
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
    CCUT_NV21_Y_CHANNEL_ONLY = 2,
    /** Use only the red channel for processing in RGB images. */
    CCUT_RGB_R_CHANNEL_ONLY = 3,
    /** Use only the green channel for processing in RGB images. */
    CCUT_RGB_G_CHANNEL_ONLY = 4,
    /** Use only the blue channel for processing in RGB images. */
    CCUT_RGB_B_CHANNEL_ONLY = 5,
}
```
