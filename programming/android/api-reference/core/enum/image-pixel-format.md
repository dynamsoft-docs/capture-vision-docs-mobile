---
layout: default-layout
title: ImagePixelFormat - Dynamsoft Core Enumerations
description: The enumeration ImagePixelFormat of Dynamsoft Core describes all supported image pixel formats.
keywords: Image pixel format
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImagePixelFormat
codeAutoHeight: true
---

# Enumeration ImagePixelFormat

`ImagePixelFormat` defines the range of pixel formats that an image can have, specifying how color and transparency data are represented in each pixel of the image.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumCapturedResultItemType
{
   /** 0:Black, 1:White. */
   int IPF_BINARY = 0;
   /** 0:White, 1:Black. */
   int IPF_BINARYINVERTED = 1;
   /** 8bit gray. */
   int IPF_GRAYSCALED = 2;
   /** NV21. */
   int IPF_NV21 = 3;
   /** 16bit with RGB channel order stored in memory from high to low address. */
   int IPF_RGB_565 = 4;
   /** 16bit with RGB channel order stored in memory from high to low address. */
   int IPF_RGB_555 = 5;
   /** 24bit with RGB channel order stored in memory from high to low address. */
   int IPF_RGB_888 = 6;
   /** 32bit with ARGB channel order stored in memory from high to low address. */
   int IPF_ARGB_8888 = 7;
   /** 48bit with RGB channel order stored in memory from high to low address. */
   int IPF_RGB_161616 = 8;
   /** 64bit with ARGB channel order stored in memory from high to low address. */
   int IPF_ARGB_16161616 = 9;
   /** 32bit with ABGR channel order stored in memory from high to low address. */
   int IPF_ABGR_8888 = 10;
   /** 64bit with ABGR channel order stored in memory from high to low address. */
   int IPF_ABGR_16161616 = 11;
   /** 24bit with BGR channel order stored in memory from high to low address. */
   int IPF_BGR_888 = 12;
   /** 0:Black, 255:White. */
   int IPF_BINARY_8 = 13;
   /** NV12 */
   int IPF_NV12 = 14;
   /** 0:white, 255:black. */
   int IPF_BINARY_8_INVERTED = 15;
}
```
