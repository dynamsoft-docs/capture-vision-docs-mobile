---
layout: default-layout
title: ImageTagType - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration ImageTagType of Dynamsoft Capture Vision iOS describes the types of image tags.
keywords: Image tag type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageTagType
codeAutoHeight: true
---

# Enumeration ImageTagType

`ImageTagType` categorizes images based on their source, distinguishing between images extracted from video streams (video frame) and those loaded from static files (file image).

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSImageTagType)
{
   /**The image tag is a DSFileImageTag.*/
   DSImageTagTypeFileImage,
   /**The image tag is a DSVideoFrameTag.*/
   DSImageTagTypeVideoFrame
};
```
>
```swift
public enum ImageTagType : Int
{
   /**The image tag is a DSFileImageTag.*/
   case fileImage
   /**The image tag is a DSVideoFrameTag.*/
   case videoFrame
}
```
