---
layout: default-layout
title: ImageSourceState - Dynamsoft Core Enumerations
description: The enumeration ImageSourceState of Dynamsoft Core describes the state of ImageSourceAdapter.
keywords: Image source state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageSourceState
codeAutoHeight: true
---
<!--Moved from Core to CVR in May 2023-->

# Enumeration ImageSourceState

`ImageSourceState` describes the state of an object that conforms to the `ImageSourceAdapter` interface and is designated as the image source in a `CaptureVisionRouter` object.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSImageSourceState)
{
   /** Indicates that the buffer of the image source is currently empty. */
   DSImageSourceStateBufferEmpty = 0,
   /** Signifies that the source for the image source has been depleted. */
   DSImageSourceStateExhausted = 1
};
```
>
```swift
public enum ImageSourceState : Int
{
   /** Indicates that the buffer of the image source is currently empty. */
   bufferEmpty = 0
   /** Signifies that the source for the image source has been depleted. */
   exhausted = 1
};
```
