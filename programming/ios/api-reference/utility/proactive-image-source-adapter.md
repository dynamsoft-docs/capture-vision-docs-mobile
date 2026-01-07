---
layout: default-layout
title: DSProactiveImageSourceAdapter - Dynamsoft Capture Vision iOS API Reference
description: The class DSProactiveImageSourceAdapter of Dynamsoft Capture Vision iOS is an abstract class that provides an interface for proactively fetching images in a separate thread.
keywords: Proactive image source adapter, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSProactiveImageSourceAdapter

The `DSProactiveImageSourceAdapter` class is an abstract base class that extends the `DSImageSourceAdapter` class. It provides an interface for proactively fetching images in a separate thread.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSProactiveImageSourceAdapter : DSImageSourceAdapter
```
2. 
```swift
class ProactiveImageSourceAdapter: ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`setImageFetchInterval`](#setimagefetchinterval) | Sets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer. |
| [`getImageFetchInterval`](#getimagefetchinterval) | Gets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer. |

### setImageFetchInterval

Sets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)setImageFetchInterval:(NSInteger)milliseconds;
```
2. 
```swift
func setImageFetchInterval(milliseconds: Int)
```

**Parameters**

`[in] milliseconds`: The time interval in milliseconds.

### getImageFetchInterval

Gets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)getImageFetchInterval;
```
2. 
```swift
func getImageFetchInterval() -> Int
```

**Return Value**

The time interval in milliseconds.
