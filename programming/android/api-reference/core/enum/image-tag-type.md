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

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageTagType
{
   public static final int ITT_FILE_IMAGE = 0;
   public static final int ITT_VIDEO_FRAME = 1;
}
```
