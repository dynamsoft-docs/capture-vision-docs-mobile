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

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSTransformMatrixType)
{
    /**Represents a transformation matrix that converts coordinates from the local image to the original image.*/
   DSTransformMatrixTypeLocalToOriginalImage = 0,
    /**Represents a transformation matrix that converts coordinates from the original image to the local image.*/
   DSTransformMatrixTypeOriginalToLocalImage = 1,
    /**Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
   DSTransformMatrixTypeRotatedToOriginalImage = 2,
    /**Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
   DSTransformMatrixTypeOriginalToRotatedImage = 3
}NS_SWIFT_NAME(TransformMatrixType);
```
>
```swift
public enum TransformMatrixType : Int
{
    /**Represents a transformation matrix that converts coordinates from the local image to the original image.*/
   localToOriginalImage = 0,
    /**Represents a transformation matrix that converts coordinates from the original image to the local image.*/
   originalToLocalImage = 1,
    /**Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
   rotatedToOriginalImage = 2,
    /**Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
   originalToRotatedImage = 3
}
```
