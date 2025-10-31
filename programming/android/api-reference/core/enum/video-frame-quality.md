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

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumVideoFrameQuality {
   /**The frame quality is measured to be high.*/
   int VFQ_HIGH = 0;
   /**The frame quality is measured to be low.*/
   int VFQ_LOW = 1;
   /**The frame quality is unknown.*/
   int VFQ_UNKNOWN = 2;
}
```
