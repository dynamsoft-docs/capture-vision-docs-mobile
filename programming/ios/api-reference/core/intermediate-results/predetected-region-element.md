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

The `DSPredetectedRegionElement` class represents a pre-detected region element, which is a subclass of `DSRegionObjectElement`.

## Definition

*Assembly:* DynamsoftCore.framework

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

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`modeName`](#modename) | *NSString \** | The name of the detection mode used to detect this region element. |

### modeName

The name of the detection mode used to detect this region element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property(nonatomic, assign, readonly) NSString *modeName;
```
2. 
```swift
var modeName: String { get }
```
