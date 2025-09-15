---
layout: default-layout
title: GrayscaleEnhancementMode - Dynamsoft Core Enumerations
description: The enumeration GrayscaleEnhancementMode of Dynamsoft Core describes all available grayscale enhancement modes.
keywords: Grayscale enhancement modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleEnhancementMode
codeAutoHeight: true
---

# Enumeration GrayscaleEnhancementMode

`GrayscaleEnhancementMode` specifies the method employed to enhance images in grayscale.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSGrayscaleEnhancementMode)
{
   /**Not supported yet. */
   DSGrayscaleEnhancementModeAuto = 1,
   /**Takes the unpreprocessed image for following operations.*/
   DSGrayscaleEnhancementModeGeneral = 2,
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   DSGrayscaleEnhancementModeGrayEqualize = 4,
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   DSGrayscaleEnhancementModeGraySmooth = 8,
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   DSGrayscaleEnhancementModeSharpenSmooth = 16,
   /**Reserved setting for image preprocessing mode.*/
   DSGrayscaleEnhancementModeRev = -2147483648,
   /**Skips image preprocessing. */
   DSGrayscaleEnhancementModeSkip = 0
};
```
>
```swift
public enum GrayscaleEnhancementMode : Int
{
   /**Not supported yet. */
   auto = 1
   /**Takes the unpreprocessed image for following operations.*/
   general = 2
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   grayEqualize = 4
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   graySmooth = 8
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   sharpenSmooth = 16
   /**Reserved setting for image preprocessing mode.*/
   rev = -2147483648
   /**Skips image preprocessing. */
   skip = 0
}
```
