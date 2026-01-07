---
layout: default-layout
title: SectionType - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration SectionType of Dynamsoft Capture Vision iOS describes the section of the algorithm.
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
   DSSectionTypeNull,
   /**The result is output by "region prediction" section.*/
   DSSectionTypeRegionPredection,
   /**The result is output by "barcode localization" section.*/
   DSSectionTypeBarcodeLocalization,
   /**The result is output by "barcode decoding" section.*/
   DSSectionTypeBarcodeDecoding,
   /**The result is output by "text line localization" section.*/
   DSSectionTypeTextLineLocalization,
   /**The result is output by "text line  recognition" section.*/
   DSSectionTypeTextLineRecognition,
   /**The result is output by "document detection" section.*/
   DSSectionTypeDocumentDetection,
   /** The section type is "document deskewing".*/
   DSSectionTypeDocumentDeskewing,
   /** The section type is "image enhancement".*/
   DSSectionTypeImageEnhancement
};
```
>
```swift
public enum SectionType : Int
{
   /**No section type is specified.*/
   case null
   /**The result is output by "region prediction" section.*/
   case regionPredection
   /**The result is output by "barcode localization" section.*/
   case barcodeLocalization
   /**The result is output by "barcode decoding" section.*/
   case barcodeDecoding
   /**The result is output by "text line localization" section.*/
   case textLineLocalization
   /**The result is output by "text line  recognition" section.*/
   case textLineRecognition
   /**The result is output by "document detection" section.*/
   case documentDetection
   /**The result is output by "document deskewing" section.*/
   case documentDeskewing
   /**The result is output by "document enhancement" section.*/
   case documentEnhancement
}
```
