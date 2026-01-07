---
layout: default-layout
title: ImageTagType - Dynamsoft Capture Vision Android Enumerations
description: The enumeration ImageTagType of Dynamsoft Capture Vision Android describes the types of image tags.
keywords: Image tag type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageTagType
codeAutoHeight: true
---

# Enumeration ImageTagType

`ImageTagType` categorizes images based on their source, distinguishing between images extracted from video streams (video frame) and those loaded from static files (file image).

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageTagType
{
   int ITT_FILE_IMAGE = 0;
   int ITT_VIDEO_FRAME = 1;
}
```
