---
layout: default-layout
title: EnumGrayscaleEnhancementMode - Dynamsoft Vision Router MAUI Edition
description: The enumeration GrayscaleEnhancementMode of Dynamsoft Vision Router specifies the method employed to enhance images in grayscale.
keywords: capture result item type, multi-frame cross filter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleEnhancementMode
---

# Enumeration GrayscaleEnhancementMode

`GrayscaleEnhancementMode` specifies the method employed to enhance images in grayscale.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
public enum EnumGrayscaleEnhancementMode
{
    /**Skips grayscale enhancement. */
    GEM_SKIP = 0,
    /**Not supported yet. */
    GEM_AUTO = 1 << 0,
    /**Takes the unpreprocessed image for following operations. */
    GEM_GENERAL = 1 << 1,
    /**Preprocesses the image using the gray equalization algorithm. Check @ref IPM for available argument settings. */
    GEM_GRAY_EQUALIZE = 1 << 2,
    /**Preprocesses the image using the gray smoothing algorithm. Check @ref IPM for available argument settings. */
    GEM_GRAY_SMOOTH = 1 << 3,
    /**Preprocesses the image using the sharpening and smoothing algorithm. Check @ref IPM for available argument settings. */
    GEM_SHARPEN_SMOOTH = 1 << 4
}
```
