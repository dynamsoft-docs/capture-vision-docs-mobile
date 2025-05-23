---
layout: default-layout
title: DSPredetectedRegionElement - Dynamsoft Core Module iOS Edition API Reference
description: The class DSPredetectedRegionElement of Dynamsoft Core Module represents a pre-detected region element, which is a subclass of DSRegionObjectElement.
keywords: pre-detected region element, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSPredetectedRegionElement

The `DSPredetectedRegionElement` class extends the `DSRegionObjectElement` class and represents a pre-detected region element in an image.

## Definition

*Assembly:* DynamsoftCore.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSPredetectedRegionElement: DSRegionObjectElement
```
2. 
```swift
class PredetectedRegionElement : RegionObjectElement
```

## Attributes

| Attributes | Description |
| ---------- | ----------- |
| [`getModeName`](#getmodename) | Gets the name of the detection mode used to detect this region element. |

### getModeName

The name of the detection mode used to detect this region element. It can be one of the following:

- "RPM_AUTO"
- "RPM_GENERAL"
- "RPM_GENERAL_RGB_CONTRAST"
- "RPM_GENERAL_GRAY_CONTRAST"
- "RPM_GENERAL_HSV_CONTRAST"

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSString *)getModeName;
```
2. 
```swift
func getModeName() -> String
```
