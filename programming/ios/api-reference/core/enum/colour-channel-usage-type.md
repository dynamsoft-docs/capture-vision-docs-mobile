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
   DSColourChannelUsageTypeAuto,
   /** Use all available color channels for processing. */
   DSColourChannelUsageTypeFullChannel,
   /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
   DSColourChannelUsageTypeYChannelOnly,
   /** Use only the red channel for processing in RGB images.*/
   DSColourChannelUsageTypeRGBRChannelOnly,
   /** Use only the green channel for processing in RGB images.*/
   DSColourChannelUsageTypeRGBGChannelOnly,
   /** Use only the blue channel for processing in RGB images.*/
   DSColourChannelUsageTypeRGBBChannelOnly
};
```
>
```swift
public enum ColourChannelUsageType : Int
{
   /** Automatic color channel usage determination based on image pixel format and scene. */
   case auto = 0
   /** Use all available color channels for processing. */
   case fullChannel = 1
   /** Use only the Y (luminance) channel for processing in images represented in the NV21 format. */
   case yChannelOnly = 2
   /** Use only the red channel for processing in RGB images.*/
   case rgbrChannelOnly = 3
   /** Use only the green channel for processing in RGB images.*/
   case rgbgChannelOnly = 4
   /** Use only the blue channel for processing in RGB images.*/
   case rgbbChannelOnly = 5
};
```
