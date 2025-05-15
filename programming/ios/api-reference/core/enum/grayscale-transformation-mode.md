---
layout: default-layout
title: GrayscaleTransformationMode - Dynamsoft Core Enumerations
description: The enumeration GrayscaleTransformationMode of Dynamsoft Core describes all available grayscale transformation modes.
keywords: Grayscale transformation modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleTransformationMode
codeAutoHeight: true
---

# Enumeration GrayscaleTransformationMode

`GrayscaleTransformationMode` specifies the method employed to transform images in grayscale.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSGrayscaleTransformationMode)
{
   /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
   DSGrayscaleTransformationModeInverted = 0x01,
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   DSGrayscaleTransformationModeOriginal = 0x02,
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   DSGrayscaleTransformationModeAuto     = 0x04,
   /** Skips grayscale transformation. */
   DSGrayscaleTransformationModeSkip     = 0x00,
   /** Reserved setting for grayscale transformation mode. */
   DSGrayscaleTransformationModeRev      = -2147483648,
   /** Placeholder value with no functional meaning. */
   DSGrayscaleTransformationModeEnd      = 0xFFFFFFFF
};
```
>
```swift
public enum GrayscaleTransformationMode : Int
{
   /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
   inverted = 0x01
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   original = 0x02
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   auto     = 0x04
   /** Skips grayscale transformation. */
   skip     = 0x00
   /** Reserved setting for grayscale transformation mode. */
   rev      = -2147483648
   /** Placeholder value with no functional meaning. */
   end      = 0xFFFFFFFF
}
```
