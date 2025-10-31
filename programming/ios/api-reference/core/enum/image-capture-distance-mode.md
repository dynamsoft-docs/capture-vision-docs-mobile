---
layout: default-layout
title: ImageCaptureDistanceMode - Dynamsoft Core Enumerations
description: The enumeration ImageCaptureDistanceMode of Dynamsoft Core is used to distinguish the close-up images from the prospect images.
keywords: Image capture distance
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageCaptureDistanceMode
codeAutoHeight: true
---

# Enumeration ImageCaptureDistanceMode

`ImageCaptureDistanceMode` describes the shooting mode of the image. It is used in the `overlap` mode of `Panorama`.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSImageCaptureDistanceMode)
{
   /** The image is taken by close-up shot camera. */
   DSImageCaptureDistanceModeNear,
   /** The image is taken by long shot camera. */
   DSImageCaptureDistanceModeFar
};
```
>
```swift
public enum ImageCaptureDistanceMode : Int
{
   /** The image is taken by close-up shot camera. */
   case near
   /** The image is taken by long shot camera. */
   case far
}
```
