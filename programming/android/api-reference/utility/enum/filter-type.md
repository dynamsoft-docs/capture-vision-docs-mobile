---
layout: default-layout
title: FilterType - Dynamsoft Capture Vision Android Enumerations
description: The enumeration FilterType of Dynamsoft Capture Vision Android edition describes the specified image filter applied to an input image.
keywords: image filter
codeAutoHeight: true
---

# Enumeration FilterType

`FilterType` describes the specified image filter applied to an input image.

```java
public @interface FilterType
{
   /**High-pass filter: Enhances edges and fine details by attenuating low-frequency components.*/
   public static final int FT_HIGH_PASS = 1；
   /**Sharpen filter: Increases contrast along edges to make the image appear more defined.*/
   public static final int FT_SHARPEN = 2；
   /**Smooth (blur) filter: Reduces noise and detail by averaging pixel values, creating a softening effect.*/
   public static final int FT_SMOOTH = 3;
}
```
