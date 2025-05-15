---
layout: default-layout
title: TargetType - Dynamsoft Core Enumerations
description: The enumeration TargetType of Dynamsoft Core describes target types.
keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TargetType
codeAutoHeight: true
---

# Enumeration TargetType

`TargetType` describes the target types.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumTargetType {
   /**The target type of the PDF file is "page". Only available for PDFReadingMode raster.*/
   public static final int TT_PAGE = 0;
   /**The target type of the PDF file is "image".*/
   public static final int TT_IMAGE = 1;
}
```
