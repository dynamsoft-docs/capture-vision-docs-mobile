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


<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSSectionType)
{
   /**No section type is specified.*/
   DSSectionTypeNull = 0,
   /**The result is output by "region prediction" section.*/
   DSSectionTypeRegionPredection = 1,
   /**The result is output by "barcode localization" section.*/
   DSSectionTypeBarcodeLocalization = 2,
   /**The result is output by "barcode decoding" section.*/
   DSSectionTypeBarcodeDecoding = 3,
   /**The result is output by "text line localization" section.*/
   DSSectionTypeTextLineLocalization = 4,
   /**The result is output by "text line  recognition" section.*/
   DSSectionTypeTextLineRecognition = 5,
   /**The result is output by "document detection" section.*/
   DSSectionTypeDocumentDetection = 6,
   /**The result is output by "document normalization" section.*/
   DSSectionTypeDocumentNormalization = 7
};
```
>
```swift
public enum SectionType : Int
{
   /**No section type is specified.*/
   null = 0,
   /**The result is output by "region prediction" section.*/
   regionPredection = 1,
   /**The result is output by "barcode localization" section.*/
   barcodeLocalization = 2,
   /**The result is output by "barcode decoding" section.*/
   barcodeDecoding = 3,
   /**The result is output by "text line localization" section.*/
   textLineLocalization = 4,
   /**The result is output by "text line  recognition" section.*/
   textLineRecognition = 5,
   /**The result is output by "document detection" section.*/
   documentDetection = 6,
   /**The result is output by "document normalization" section.*/
   documentNormalization = 7
}
```
