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

## Methods

| Method | Description |
| ------ | ----------- |
| [`getModeName`](#getmodename) | Gets the name of the detection mode used to detect this region element. |
| [`setLocation`](#setlocation) | Sets the location of the pre-detected region object. |
| [`getLabelId`](#getlabelid) | Gets the label ID of the pre-detected region object. |
| [`getLabelName`](#getlabelname) | Gets the label name of the pre-detected region object. |

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

**Return Value**

The name of the detection mode used to detect this region element.

### setLocation

Sets the location of the pre-detected region object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)setLocation:(DSQuadrilateral *)location;
```
2. 
```swift
func setLocation(_ location: Quadrilateral?)
```

**Parameters**

`location`: The location info of the element that defined in DSQuadrilateral.

**Return Value**

The location info of the element that defined in DSQuadrilateral.

### getLabelId

Gets the label ID of this pre-detected region.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)getLabelId;
```
2. 
```swift
func getLabelId() -> Int
```

**Return Value**

The label ID of this pre-detected region.

### getLabelName

Gets the label name of this pre-detected region element.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSString *)getLabelName;
```
2. 
```swift
func getLabelName() -> String
```

**Return Value**

The label name of this pre-detected region element.
