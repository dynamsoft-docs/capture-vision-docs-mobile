---
layout: default-layout
title: TransformMatrixType - Dynamsoft Core Enumerations
description: The enumeration TransformMatrixType of Dynamsoft Core describes transform matrix types.
keywords: Target type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TransformMatrixType
---

# Enumeration TransformMatrixType

`TransformMatrixType` describes the transform matrix types.

```java
public @interface EnumTransformMatrixType {
    /**Represents a transformation matrix that converts coordinates from the local image to the original image.*/
    int TMT_LOCAL_TO_ORIGINAL_IMAGE = 0;
    /**Represents a transformation matrix that converts coordinates from the original image to the local image.*/
    int TMT_ORIGINAL_TO_LOCAL_IMAGE = 1;
    /**Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
    int TMT_ROTATED_TO_ORIGINAL_IMAGE = 2;
    /**Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
    int TMT_ORIGINAL_TO_ROTATED_IMAGE = 3;
    /**Represents a transformation matrix that converts coordinates from the local image to the section image.*/
    int TMT_LOCAL_TO_SECTION_IMAGE = 4;
    /**Represents a transformation matrix that converts coordinates from the section image to the local image.*/
    int TMT_SECTION_TO_LOCAL_IMAGE = 5;
}
```
