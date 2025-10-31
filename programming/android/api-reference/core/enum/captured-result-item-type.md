---
layout: default-layout
title: CapturedResultItemType - Dynamsoft Core Enumerations
description: The enumeration CapturedResultItemType of Dynamsoft Core describes all types of captured result item.
keywords: Captured result types
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CapturedResultItemType
codeAutoHeight: true
---

# Enumeration CapturedResultItemType

`CapturedResultItemType` defines the various categories of items that can be recognized and captured.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumCapturedResultItemType
{
   /** The type of the CapturedResultItem is "original image". */
   int CRIT_ORIGINAL_IMAGE = 1;
   /** The type of the CapturedResultItem is "barcode". */
   int CRIT_BARCODE = 2;
   /** The type of the CapturedResultItem is "text line". */
   int CRIT_TEXT_LINE = 4;
   /** The type of the CapturedResultItem is "detected quad". */
   int CRIT_DETECTED_QUAD = 8;
   /** The type of the CapturedResultItem is "deskewed image". */
   int CRIT_DESKEWED_IMAGE = 16;
   /** The type of the CapturedResultItem is "parsed result". */
   int CRIT_PARSED_RESULT = 32;
   /** The type of the CapturedResultItem is "enhanced image". */
   int CRIT_ENHANCED_IMAGE = 64;
}
```
