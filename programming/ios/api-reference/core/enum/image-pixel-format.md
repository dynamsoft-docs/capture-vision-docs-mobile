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

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSImagePixelFormat)
{
   /** 0:black, 1:white */
   DSImagePixelFormatBinary,
   /** 0:white, 1:black */
   DSImagePixelFormatBinaryInverted,
   /** 8-bit gray */
   DSImagePixelFormatGrayScaled,
   /** NV21 */
   DSImagePixelFormatNV21,
   /** 16bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB_565,
   /** 16bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB_555,
   /** 24bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB_888,
   /** 32bit with ARGB channel order stored in memory from high to low address*/
   DSImagePixelFormatARGB_8888,
   /** 48bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB_161616,
   /** 64bit with ARGB channel order stored in memory from high to low address*/
   DSImagePixelFormatARGB_16161616,
   /** 32bit with ABGB channel order stored in memory from high to low address */
   DSImagePixelFormatABGR_8888,
   /** 64bit with ABGR channel order stored in memory from high to low address*/
   DSImagePixelFormatABGR_16161616,
   /** 24bit with BGR channel order stored in memory from high to low address*/
   DSImagePixelFormatBGR_888,
   /**  0:black, 255:white */
   DSImagePixelFormatBinary_8,
   /**NV12 */
   DSImagePixelFormatNV12
};
```
>
```swift
public enum ImagePixelFormat : Int
{
   /** 0:black, 1:white */
   binary
   /** 0:white, 1:black */
   binaryInverted
   /** 8-bit gray */
   grayScaled
   /** NV21 */
   NV21
   /** 16bit with RGB channel order stored in memory from high to low address*/
   RGB_565
   /** 16bit with RGB channel order stored in memory from high to low address*/
   RGB_555
   /** 24bit with RGB channel order stored in memory from high to low address*/
   RGB_888
   /** 32bit with ARGB channel order stored in memory from high to low address*/
   ARGB_8888
   /** 48bit with RGB channel order stored in memory from high to low address*/
   RGB_161616
   /** 64bit with ARGB channel order stored in memory from high to low address*/
   ARGB_16161616
   /** 32bit with ABGB channel order stored in memory from high to low address */
   ABGR_8888
   /** 64bit with ABGR channel order stored in memory from high to low address*/
   ABGR_16161616
   /** 24bit with BGR channel order stored in memory from high to low address*/
   BGR_888
   /**  0:black, 255:white */
   binary8
   /**NV12 */
   NV12
}
```
