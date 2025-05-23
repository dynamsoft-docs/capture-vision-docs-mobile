---
layout: default-layout
title: SectionType - Dynamsoft Core Enumerations
description: The enumeration SectionType of Dynamsoft Core describes the section of the algorithm.
keywords: Section type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: SectionType
codeAutoHeight: true
---

# Enumeration SectionType

`SectionType` categorizes the distinct segments within the image processing algorithm, pinpointing the exact phase responsible for generating a specific `IntermediateResult`.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumSectionType
{
   /**No section type is specified.*/
   public static final int ST_NULL = 0;
   /**The result is output by "region prediction" section.*/
   public static final int ST_REGION_PREDETECTION = 1;
   /**The result is output by "barcode localization" section.*/
   public static final int ST_BARCODE_LOCALIZATION = 2;
   /**The result is output by "barcode decoding" section.*/
   public static final int ST_BARCODE_DECODING = 3;
   /**The result is output by "text line localization" section.*/
   public static final int ST_TEXT_LINE_LOCALIZATION = 4;
   /**The result is output by "text line  recognition" section.*/
   public static final int ST_TEXT_LINE_RECOGNITION = 5;
   /**The result is output by "document detection" section.*/
   public static final int ST_DOCUMENT_DETECTION = 6;
   /**The result is output by "document normalization" section.*/
   public static final int ST_DOCUMENT_NORMALIZATION = 7;
}
```
