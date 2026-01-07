---
layout: default-layout
title: GrayscaleEnhancementMode - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration GrayscaleEnhancementMode of Dynamsoft Capture Vision iOS describes all available grayscale enhancement modes.
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
   /**Skips image preprocessing. */
   DSGrayscaleEnhancementModeSkip = 0,
   /**Not supported yet. */
   DSGrayscaleEnhancementModeAuto = 1 << 0,
   /**Takes the unpreprocessed image for following operations.*/
   DSGrayscaleEnhancementModeGeneral = 1 << 1,
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   DSGrayscaleEnhancementModeGrayEqualize = 1 << 2,
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   DSGrayscaleEnhancementModeGraySmooth = 1 << 3,
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   DSGrayscaleEnhancementModeSharpenSmooth = 1 << 4,
   /**Placeholder value with no functional meaning. */
   DSGrayscaleEnhancementModeEnd = -1,
   /**Reserved setting for image preprocessing mode.*/
   DSGrayscaleEnhancementModeRev = NSIntegerMin
};
```
>
```swift
public enum GrayscaleEnhancementMode : Int
{
   /**Skips image preprocessing. */
   case skip = 0
   /**Not supported yet. */
   case auto = 1 << 0
   /**Takes the unpreprocessed image for following operations.*/
   case general = 1 << 1
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   case grayEqualize = 1 << 2
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   case graySmooth = 1 << 3
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   case sharpenSmooth = 1 << 4
   /**Placeholder value with no functional meaning. */
   case end = -1
   /**Reserved setting for image preprocessing mode.*/
   case rev = Int.min
}
```
