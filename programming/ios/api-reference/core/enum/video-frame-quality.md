---
layout: default-layout
title: VideoFrameQuality - Dynamsoft Core Enumerations
description: The enumeration VideoFrameQuality of Dynamsoft Core describes the quality of video frames.
keywords: Video frame quality
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: VideoFrameQuality
codeAutoHeight: true
---

# Enumeration VideoFrameQuality

`VideoFrameQuality` describes the quality of video frames.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSFrameQuality)
{
   /**The frame quality is measured to be high.*/
   FrameQualityHIGH,
   /**The frame quality is measured to be low.*/
   FrameQualityLOW,
   /**The frame quality is unknown.*/
   FrameQualityUNKNOWN
};
```
>
```swift
public enum VideoFrameQuality : Int
{
   /**The frame quality is measured to be high.*/
   case high
   /**The frame quality is measured to be low.*/
   case low
   /**The frame quality is unknown.*/
   case unknown
}
```
