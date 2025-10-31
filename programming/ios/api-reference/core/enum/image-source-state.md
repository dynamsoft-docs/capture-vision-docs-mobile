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
ignore: true
---
<!--Moved from Core to CVR in May 2023-->

# Enumeration ImageSourceState

`ImageSourceState` describes the state of `ImageSourceAdapter`.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSImageSourceState)
{
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   DSImageSourceStateBufferEmpty = 0,
   /** The source of ImageSourceAdapter is empty. */
   DSImageSourceStateExhausted = 1
};
```
>
```swift
public enum ImageSourceState : Int
{
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   case bufferEmpty = 0
   /** The source of ImageSourceAdapter is empty. */
   case exhausted = 1
};
```
