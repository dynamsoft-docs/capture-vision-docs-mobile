---
layout: default-layout
title: PDFReadingMode - Dynamsoft Core Enumerations
description: The enumeration PDFReadingMode of Dynamsoft Core describes all available PDF reading modes.
keywords: PDF Reading Mode
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: PDFReadingMode
codeAutoHeight: true
---

# Enumeration PDFReadingMode

`PDFReadingMode` describes the PDF reading modes.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumPDFReadingMode
{
   /** Capture content from vector data in PDF file. */
   public static final int PDFRM_VECTOR = 1;
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   public static final int PDFRM_RASTER = 2;
   /** Reserved setting for PDF reading mode.*/
   public static final int PDFRM_REV = -2147483648;
}
```
