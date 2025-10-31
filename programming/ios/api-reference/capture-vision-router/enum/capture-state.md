---
layout: default-layout
title: CaptureState - Dynamsoft Vision Router Enumerations
description: The enumeration CaptureState of Dynamsoft Vision Router describes the state of data capturing.
keywords: Capture state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CaptureState
---

# Enumeration CaptureState

`CaptureState` describes the state of data capturing.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSCaptureState)
{
   /** The data capturing is started. */
   DSCaptureStateStarted,
   /** The data capturing is stopped. */
   DSCaptureStateStopped,
   /** The data capturing is paused. */
   DSCaptureStatePaused
};
```
>
```swift
public enum CaptureState : Int
{
   /** The data capturing is started. */
   started
   /** The data capturing is stopped. */
   stopped
   /** The data capturing is paused. */
   paused
};
```
