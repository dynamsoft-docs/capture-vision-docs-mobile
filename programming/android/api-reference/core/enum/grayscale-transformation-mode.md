---
layout: default-layout
title: GrayscaleTransformationMode - Dynamsoft Capture Vision Android Enumerations
description: The enumeration GrayscaleTransformationMode of Dynamsoft Capture Vision Android describes all available grayscale transformation modes.
keywords: Grayscale transformation modes
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleTransformationMode
codeAutoHeight: true
---

# Enumeration GrayscaleTransformationMode

`GrayscaleTransformationMode` specifies the method employed to transform images in grayscale.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumGrayscaleTransformationMode
{
   /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
   int GTM_INVERTED = 1;
   /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
   int GTM_ORIGINAL = 2;
   /**Lets the library choose an algorithm automatically for grayscale transformation.*/
   int GTM_AUTO = 4;
   /** Skips grayscale transformation. */
   int GTM_SKIP = 0;
   /** Reserved setting for grayscale transformation mode. */
   int GTM_REV = -2147483648;
   /**Placeholder value with no functional meaning. */
   int GTM_END = 0xFFFFFFFF;
}
```
