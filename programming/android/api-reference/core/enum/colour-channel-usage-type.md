---
layout: default-layout
title: ColourChannelUsageType - Dynamsoft Core Enumerations
description: The enumeration ColourChannelUsageType of Dynamsoft Core describes how the color channel is used in the image.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ColourChannelUsageType
codeAutoHeight: true
---

# Enumeration ColourChannelUsageType

`ColourChannelUsageType` enumerates the different ways color channels can be utilized in image processing. This allows for flexible image analysis and manipulation by specifying how color data should be handled.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumColourChannelUsageType
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
    public static final int CCUT_AUTO = 0;
    /** Use all available color channels for processing. */
    public static final int CCUT_FULL_CHANNEL = 1;
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
    public static final int CCUT_NV21_Y_CHANNEL_ONLY = 2;
    /** Use only the red channel for processing in RGB images.*/
    public static final int CCUT_RGB_R_CHANNEL_ONLY = 3;
    /** Use only the green channel for processing in RGB images.*/
    public static final int CCUT_RGB_G_CHANNEL_ONLY = 4;
    /** Use only the blue channel for processing in RGB images.*/
    public static final int CCUT_RGB_B_CHANNEL_ONLY = 5;
}
```
