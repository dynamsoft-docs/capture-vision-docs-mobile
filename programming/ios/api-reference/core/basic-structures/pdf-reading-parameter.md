---
layout: default-layout
title: DSPDFReadingParameter - Dynamsoft Core Module iOS Edition API Reference
description: The class DSPDFReadingParameter of Dynamsoft Core Module represents the parameters for reading a PDF file, including the mode of PDF reading, the DPI (dots per inch) value, and the data source type.
keywords: PDF reading parameter, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# DSPDFReadingParameter

The `DSPDFReadingParameter` class represents the parameters for reading a PDF file, including the mode of PDF reading, the DPI (dots per inch) value, and the data source type.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSPDFReadingParameter : NSObject
```
2. 
```swift
class PDFReadingParameter : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`mode`](#mode) | *DSPDFReadingMode* | Set the processing mode of the PDF file. You can either read the PDF info from vector data or transform the PDF file into an image. The library will transform the PDF file into an image by default. |
| [`dpi`](#dpi) | *NSInteger* | Set the DPI (dots per inch) of the PDF file. |
| [`rasterDataSource`](#rasterdatasource) | *DSRasterDataSource* | Set the data source type of the image. The default type is pages. |

### mode

Set the processing mode of the PDF file. You can either read the PDF info from vector data or transform the PDF file into an image. The library will transform the PDF file into an image by default.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign) DSPDFReadingMode mode;
```
2. 
```swift
var mode: PDFReadingMode { get set }
```

### dpi

Set the DPI (dots per inch) of the PDF file.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign) NSInteger dpi;
```
2. 
```swift
var dpi: Int { get set }
```

### rasterDataSource

Set the raster data source type of the image. The default type is pages.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign) DSRasterDataSource rasterDataSource;
```
2. 
```swift
var rasterDataSource: DSRasterDataSource { get set }
```
