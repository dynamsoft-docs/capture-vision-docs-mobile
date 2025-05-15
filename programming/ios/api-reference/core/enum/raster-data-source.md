---
layout: default-layout
title: RasterDataSource - Dynamsoft Core Enumerations
description: The enumeration RasterDataSource of Dynamsoft Core describes raster data source types.
keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RasterDataSource
---

# Enumeration RasterDataSource

`RasterDataSource` describes the target types.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSRasterDataSource)
{
   /**The raster data source type of the PDF file is "pages". Only available for PDFReadingMode raster.*/
   DSRasterDataSourceRasterizedPages = 0,
   /**The raster data source type of the PDF file is "images".*/
   DSRasterDataSourceExtractedImages = 1
}NS_SWIFT_NAME(RasterDataSource);
```
>
```swift
public enum RasterDataSource : Int
{
   /**The raster data source type of the PDF file is "pages". Only available for PDFReadingMode raster.*/
   rasterizedPages = 0,
   /**The raster data source type of the PDF file is "images".*/
   extractedImages = 1
}
```
