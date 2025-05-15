---
layout: default-layout
title: BufferOverflowProtectionMode - Dynamsoft Core Enumerations
description: The enumeration BufferOverflowProtectionMode of Dynamsoft Core describes the protection modes when the buffer of ImageSourceAdapter is overflow.
keywords: Buffer overflow protection mode 
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BufferOverflowProtectionMode
codeAutoHeight: true
---

# Enumeration BufferOverflowProtectionMode

`BufferOverflowProtectionMode` describes the protection modes to manage situations when the `ImageSourceAdapter`'s buffer exceeds its capacity. 

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSBufferOverflowProtectionMode)
{
   /** New images are blocked when the buffer is full.*/
   DSBufferOverflowProtectionModeBlock = 0,
   /** New images are appended at the end, and oldest images are pushed out from the beginning if thebuffer is full.*/
   DSBufferOverflowProtectionModeUpdate = 1,
}NS_SWIFT_NAME(BufferOverflowProtectionMode);
```
>
```swift
public enum BufferOverflowProtectionMode : Int
{
   /** New images are blocked when the buffer is full.*/
   block = 0
   /** New images are appended at the end, and oldest images are pushed out from the beginning if thebuffer is full.*/
   update = 1
}
```
