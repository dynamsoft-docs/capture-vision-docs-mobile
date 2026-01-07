---
layout: default-layout
title: GrayscaleTransformationMode - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration GrayscaleTransformationMode of Dynamsoft Capture Vision iOS describes all available grayscale transformation modes.
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
   /** Skips grayscale transformation. */
   DSGrayscaleTransformationModeSkip     = 0,
   /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
   DSGrayscaleTransformationModeInverted = 1 << 0,
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   DSGrayscaleTransformationModeOriginal = 1 << 1,
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   DSGrayscaleTransformationModeAuto     = 1 << 2,
   /** Placeholder value with no functional meaning. */
   DSGrayscaleTransformationModeEnd      = -1,
   /** Reserved setting for grayscale transformation mode. */
   DSGrayscaleTransformationModeRev      = NSIntegerMin
};
```
>
```swift
public enum GrayscaleTransformationMode : Int
{
   /** Skips grayscale transformation. */
   case skip     = 0
   /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
   case inverted = 1 << 0
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   case original = 1 << 1
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   case auto     = 1 << 2
   /** Placeholder value with no functional meaning. */
   case end      = -1
   /** Reserved setting for grayscale transformation mode. */
   case rev      = Int.min
}
```
