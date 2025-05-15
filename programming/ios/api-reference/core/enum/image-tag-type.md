---
layout: default-layout
title: ImageTagType - Dynamsoft Core Enumerations
description: The enumeration ImageTagType of Dynamsoft Core describes the types of image tags.
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
   DSImageTagTypeFileImage = 0,
   /**The image tag is a DSVideoFrameTag.*/
   DSImageTagTypeVideoFrame = 1,
};
```
>
```swift
public enum ImageTagType : Int
{
   /**The image tag is a DSFileImageTag.*/
   fileImage = 0,
   /**The image tag is a DSVideoFrameTag.*/
   videoFrame = 1,
}
```
