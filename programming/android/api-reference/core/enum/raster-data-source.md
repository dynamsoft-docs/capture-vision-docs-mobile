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

```java
public @interface EnumRasterDataSource {
   /**The raster data source type of the PDF file is "pages". Only available for PDFReadingMode raster.*/
   public static final int RDS_RASTERIZED_PAGES = 0;
   /**The raster data source type of the PDF file is "images".*/
   public static final int RDS_EXTRACTED_IMAGES = 1;
}
```
