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
    /** Lets the Library choose the reading mode automatically. Not supported yet. */
    int PDFRM_AUTO = 0x01;
   /** Capture content from vector data in PDF file. */
   int PDFRM_VECTOR = 0x02;
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   int PDFRM_RASTER = 0x02;
   /** Reserved setting for PDF reading mode.*/
   int PDFRM_REV = -2147483648;
}
```
