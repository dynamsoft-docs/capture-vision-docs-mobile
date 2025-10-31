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
   DSImagePixelFormatRGB565,
   /** 16bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB555,
   /** 24bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB888,
   /** 32bit with ARGB channel order stored in memory from high to low address*/
   DSImagePixelFormatARGB8888,
   /** 48bit with RGB channel order stored in memory from high to low address*/
   DSImagePixelFormatRGB161616,
   /** 64bit with ARGB channel order stored in memory from high to low address*/
   DSImagePixelFormatARGB16161616,
   /** 32bit with ABGB channel order stored in memory from high to low address */
   DSImagePixelFormatABGR8888,
   /** 64bit with ABGR channel order stored in memory from high to low address*/
   DSImagePixelFormatABGR16161616,
   /** 24bit with BGR channel order stored in memory from high to low address*/
   DSImagePixelFormatBGR888,
   /**  0:black, 255:white */
   DSImagePixelFormatBinary8,
   /**NV12 */
   DSImagePixelFormatNV12,
   /** 0:white, 255:black */
   DSImagePixelFormatBinary8Inverted
};
```
>
```swift
public enum ImagePixelFormat : Int
{
   /** 0:black, 1:white */
   case binary
   /** 0:white, 1:black */
   case binaryInverted
   /** 8-bit gray */
   case grayScaled
   /** NV21 */
   case NV21
   /** 16bit with RGB channel order stored in memory from high to low address*/
   case RGB565
   /** 16bit with RGB channel order stored in memory from high to low address*/
   case RGB555
   /** 24bit with RGB channel order stored in memory from high to low address*/
   case RGB888
   /** 32bit with ARGB channel order stored in memory from high to low address*/
   case ARGB8888
   /** 48bit with RGB channel order stored in memory from high to low address*/
   case RGB161616
   /** 64bit with ARGB channel order stored in memory from high to low address*/
   case ARGB16161616
   /** 32bit with ABGB channel order stored in memory from high to low address */
   case ABGR8888
   /** 64bit with ABGR channel order stored in memory from high to low address*/
   case ABGR16161616
   /** 24bit with BGR channel order stored in memory from high to low address*/
   case BGR888
   /**  0:black, 255:white */
   case binary8
   /**NV12 */
   case NV12
   /**NV12 */
   case binary8Inverted
}
```
