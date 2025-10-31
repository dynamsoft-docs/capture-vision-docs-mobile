---
layout: default-layout
title: BinarizationMode - Dynamsoft Core Enumerations
description: The enumeration BinarizationMode of Dynamsoft Core describes how the corner is formed by its sides.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BinarizationMode
codeAutoHeight: true
---

# Enumeration BinarizationMode

`BinarizationMode` categorizes the nature of a corner based on the intersection of its adjoining sides.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumBinarizationMode
{
    /** Binarizes the image based on the local block. Check @ref BM for available argument settings.*/
    int BM_LOCAL_BLOCK = 0x02;

    /** Performs image binarization based on the given threshold. Check @ref BM for available argument settings.*/
    int BM_THRESHOLD = 0x04;

    /** Skips the binarization.*/
    int BM_SKIP = 0x00;

    /** Reserved settings for the binarization mode.*/
    int BM_REV = -2147483648;
}
```
