---
layout: default-layout
title: ImagePixelFormat - Dynamsoft Core Enumerations
description: The enumeration ImagePixelFormat of Dynamsoft Core defines the file format of the image file.
keywords: Image file format
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImagePixelFormat
codeAutoHeight: true
---

# Enumeration ImagePixelFormat

`ImagePixelFormat` defines the file format of the image file.

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
public enum ImagePixelFormat : Int
{
    case jpeg = 0
    case png = 1
    case bmp = 2
    case pdf = 3
}
```
