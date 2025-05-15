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

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSColourChannelUsageType)
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
    DSColourChannelUsageTypeAuto = 0,
    /** Use all available color channels for processing. */
    DSColourChannelUsageTypeFullChannel = 1,
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
    DSColourChannelUsageTypeNV21YChannelOnly = 2,
    /** Use only the red channel for processing in RGB images.*/
    DSColourChannelUsageTypeRGBRChannelOnly = 3,
    /** Use only the green channel for processing in RGB images.*/
    DSColourChannelUsageTypeRGBGChannelOnly = 4,
    /** Use only the blue channel for processing in RGB images.*/
    DSColourChannelUsageTypeRGBBChannelOnly = 5
};
```
>
```swift
public enum ColourChannelUsageType : Int
{
    /** Automatic color channel usage determination based on image pixel format and scene. */
   auto = 0,
    /** Use all available color channels for processing. */
   fullChannel = 1,
    /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
   nv21YChannelOnly = 2,
    /** Use only the red channel for processing in RGB images.*/
   rgbrChannelOnly = 3,
    /** Use only the green channel for processing in RGB images.*/
   rgbgChannelOnly = 4,
    /** Use only the blue channel for processing in RGB images.*/
   rgbbChannelOnly = 5
};
```
