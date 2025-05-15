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

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSPDFReadingMode)
{
   /** Capture content from vector data in PDF file. */
   DSPDFReadingModeVector = 0x01,
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   DSPDFReadingModeRaster = 0x02,
   /** Reserved setting for PDF reading mode.*/
   DSPDFReadingModeRev = -2147483648
};
```
>
```swift
public enum PDFReadingMode : Int
{
   /** Capture content from vector data in PDF file. */
   vector = 0x01,
   /** The default value.
    * Outputs raster data found in the PDFs.
    * Depending on the argument Resolution, the SDK may rasterize the PDF pages.
    * Check the template for available argument settings. */
   raster = 0x02,
   /** Reserved setting for PDF reading mode.*/
   rev = -2147483648
};
```
