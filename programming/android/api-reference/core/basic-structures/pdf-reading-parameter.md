---
layout: default-layout
title: PDFReadingParameter - Dynamsoft Core Module Android Edition API Reference
description: The class PDFReadingParameter of Dynamsoft Core Module represents the parameters for reading a PDF file, including the mode of PDF reading, the DPI (dots per inch) value, and the data source type.
keywords: PDF reading parameter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# PDFReadingParameter

The `PDFReadingParameter` class represents the parameters for reading a PDF file, including the mode of PDF reading, the DPI (dots per inch) value, and the data source type.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class PDFReadingParameter
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`mode`](#mode) | *int* | Set the processing mode of the PDF file. You can either read the PDF info from vecter data or transform the PDF file into an image. The library will transform the PDF file into an image by default. |
| [`dpi`](#dpi) | *int* | Set the DPI (dots per inch) of the PDF file. |
| [`rasterDataSource`](#rasterdatasource) | *int* | Set the raster data source type of the image. The default type is [`RDS_RASTERIZED_PAGES`]({{ site.dcv_android_api }}core/enum/raster-data-source.html). |

### mode

Set the processing mode of the PDF file. You can either read the PDF info from vector data or transform the PDF file into an image. The library will transform the PDF file into an image by default.

```java
int mode;
```

### dpi

Set the DPI (dots per inch) of the PDF file.

```java
int dpi;
```

### rasterDataSource

Set the raster data source type of the image. The default type is [`RDS_RASTERIZED_PAGES`]({{ site.dcv_android_api }}core/enum/raster-data-source.html).

```java
int rasterDataSource;
```
