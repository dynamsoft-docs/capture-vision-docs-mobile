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
   /** Represents a transformation matrix that converts coordinates from the local image to the original image.*/
   DSTransformMatrixTypeLocalToOriginalImage,
   /** Represents a transformation matrix that converts coordinates from the original image to the local image.*/
   DSTransformMatrixTypeOriginalToLocalImage,
   /** Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
   DSTransformMatrixTypeRotatedToOriginalImage,
   /** Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
   DSTransformMatrixTypeOriginalToRotatedImage,
   /** Represents a transformation matrix that converts coordinates from the local image to the section image.*/
   DSTransformMatrixTypeLocalToSectionImage,
   /** Represents a transformation matrix that converts coordinates from the section image to the local image.*/
   DSTransformMatrixTypeSectionToLocalImage
}NS_SWIFT_NAME(TransformMatrixType);
```
>
```swift
public enum TransformMatrixType : Int
{
   /**Represents a transformation matrix that converts coordinates from the local image to the original image.*/
   case localToOriginalImage
   /**Represents a transformation matrix that converts coordinates from the original image to the local image.*/
   case originalToLocalImage
   /**Represents a transformation matrix that converts coordinates from the rotated image to the original image.*/
   case rotatedToOriginalImage
   /**Represents a transformation matrix that converts coordinates from the original image to the rotated image.*/
   case originalToRotatedImage
   /** Represents a transformation matrix that converts coordinates from the local image to the section image.*/
   case localToSectionImage
   /** Represents a transformation matrix that converts coordinates from the section image to the local image.*/
   case sectionToLocalImage
}
```
