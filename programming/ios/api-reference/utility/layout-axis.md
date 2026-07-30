---
layout: default-layout
title: DSLayoutAxis - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSLayoutAxis of Dynamsoft Capture Vision iOS edition provides axis configuration for layout analysis.
keywords: layout axis, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLayoutAxis

The `DSLayoutAxis` class provides configuration for a single axis in layout analysis.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(LayoutAxis)
@interface DSLayoutAxis : NSObject
```
2. 
```swift
class LayoutAxis : NSObject
```

## Attributes

| Attribute | Type | Description |
| --------- | ---- | ----------- |
| [`elementCount`](#elementcount) | *NSInteger* | Expected number of elements along this axis. Use -1 for auto-detection. |
| [`isStaggered`](#isstaggered) | *BOOL* | Whether the layout uses an offset/staggered pattern. |
| [`angle`](#angle) | *NSInteger* | Target angle [0, 180]. Use -1 for auto-detection. |
| [`isEqualSpacing`](#isequalspacing) | *BOOL* | Force equal gaps between elements. When false, spacing is ignored. |
| [`spacing`](#spacing) | *NSInteger* | Spacing between elements along this axis. Use -1 for auto-detection. |
| [`spacingUnit`](#spacingunit) | *DSMeasureUnit* | Interpretation mode for the spacing value. |

### elementCount

Expected number of elements along this axis. Use -1 for auto-detection.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger elementCount;
```
2. 
```swift
var elementCount: Int { get set }
```

### isStaggered

Whether the layout uses an offset/staggered pattern.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) BOOL isStaggered;
```
2. 
```swift
var isStaggered: Bool { get set }
```

### angle

Target angle [0, 180]. Use -1 for auto-detection.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger angle;
```
2. 
```swift
var angle: Int { get set }
```

### isEqualSpacing

Force equal gaps between elements. When false, spacing is ignored.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) BOOL isEqualSpacing;
```
2. 
```swift
var isEqualSpacing: Bool { get set }
```

### spacing

Spacing between elements along this axis. Use -1 for auto-detection.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger spacing;
```
2. 
```swift
var spacing: Int { get set }
```

### spacingUnit

Interpretation mode for the spacing value.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) DSMeasureUnit spacingUnit;
```
2. 
```swift
var spacingUnit: MeasureUnit { get set }
```
