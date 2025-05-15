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
typedef NS_ENUM(NSInteger, DSVideoFrameQuality)
{
   /**The frame quality is measured to be high.*/
   VideoFrameQualityHigh,
   /**The frame quality is measured to be low.*/
   VideoFrameQualityLow,
   /**The frame quality is unknown.*/
   VideoFrameQualityUnknown
};
```
>
```swift
public enum VideoFrameQuality : Int
{
   /**The frame quality is measured to be high.*/
   high,
   /**The frame quality is measured to be low.*/
   low,
   /**The frame quality is unknown.*/
   unknown
}
```
