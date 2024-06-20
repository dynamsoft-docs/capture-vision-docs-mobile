---
layout: default-layout
title: EnumGrayscaleTransformationMode - Dynamsoft Vision Router MAUI Edition
description: The enumeration GrayscaleTransformationMode of Dynamsoft Vision Router specifies the method employed to transform images in grayscale.
keywords: capture result item type, multi-frame cross filter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: GrayscaleTransformationMode
---

# Enumeration GrayscaleTransformationMode

`GrayscaleTransformationMode` specifies the method employed to transform images in grayscale.

## Definition

*Namespace:* Dynamsoft.Core.Maui

*Assembly:* Dynamsoft.Core.Maui

```csharp
public enum EnumGrayscaleTransformationMode
{
    /** Skips grayscale transformation. */
    GTM_SKIP = 0,
    /** Transforms to the inverted grayscale for further reference. This value is recommended for light on dark images. */
    GTM_INVERTED = 1 << 0,
    /** Keeps the original grayscale for further reference. This value is recommended for dark on light images. */
    GTM_ORIGINAL = 1 << 1,
    /**Lets the library choose an algorithm automatically for grayscale transformation. */
    GTM_AUTO = 1 << 2
}
```
