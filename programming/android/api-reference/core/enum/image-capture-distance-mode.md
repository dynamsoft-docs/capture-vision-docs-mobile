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

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageCaptureDistanceMode
{
   /** The image is taken by close-up shot camera. */
   int ICDM_NEAR = 0;
   /** The image is taken by long shot camera. */
   int ICDM_FAR = 1;
}
```
