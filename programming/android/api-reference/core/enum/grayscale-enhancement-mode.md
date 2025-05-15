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

```java
@Retention(RetentionPolicy.CLASS)public @interface EnumGrayscaleEnhancementMode {
   /**Not supported yet. */
   public static final int GEM_AUTO = 1;
   /**Takes the unpreprocessed image for following operations.*/
   public static final int GEM_GENERAL = 2;
   /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings.*/
   public static final int GEM_GRAY_EQUALIZE = 4;
   /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings.*/
   public static final int GEM_GRAY_SMOOTH = 8;
   /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings.*/
   public static final int GEM_SHARPEN_SMOOTH = 16;
   /**Reserved setting for image preprocessing mode.*/
   public static final int GEM_REV = -2147483648;
   /**Skips image preprocessing. */
   public static final int GEM_SKIP = 0;
   /**Placeholder value with no functional meaning. */
   public static final int GEM_END = 0xFFFFFFFF;
}
```
