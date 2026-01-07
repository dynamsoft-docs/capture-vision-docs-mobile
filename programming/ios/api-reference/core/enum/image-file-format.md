---
layout: default-layout
title: ImageFileFormat - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration ImageFileFormat of Dynamsoft Capture Vision iOS defines the file format of the image file.
keywords: Image file format
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageFileFormat
codeAutoHeight: true
---

# Enumeration ImageFileFormat

`ImageFileFormat` defines the file format of the image file.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSImageFileFormat)
{
    DSImageFileFormatJPEG = 0,
    DSImageFileFormatPNG = 1,
    DSImageFileFormatBMP = 2,
    DSImageFileFormatPDF = 3
};
```
>
```swift
public enum ImageFileFormat : Int
{
    case jpeg = 0
    case png = 1
    case bmp = 2
    case pdf = 3
}
```
