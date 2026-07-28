---
layout: default-layout
title: DSLayoutAnalysisParameter - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSLayoutAnalysisParameter of Dynamsoft Capture Vision iOS edition provides parameters for layout analysis.
keywords: layout analysis parameter, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLayoutAnalysisParameter

The `DSLayoutAnalysisParameter` class provides parameters to constrain the layout analysis.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(LayoutAnalysisParameter)
@interface DSLayoutAnalysisParameter : NSObject
```
2. 
```swift
class LayoutAnalysisParameter : NSObject
```

## Attributes

| Attribute | Type | Description |
| --------- | ---- | ----------- |
| [`pattern`](#pattern) | *DSLayoutPattern* | Desired layout pattern. Use DSLayoutPatternUnknown for auto-detection. |
| [`axes`](#axes) | *NSArray<DSLayoutAxis \*> \** | Configuration for primary axis [0] and secondary axis [1]. |
| [`inputImageWidth`](#inputimagewidth) | *NSInteger* | Width of the reference image. Required when spacingUnit is MU_PERCENTAGE. |
| [`inputImageHeight`](#inputimageheight) | *NSInteger* | Height of the reference image. Required when spacingUnit is MU_PERCENTAGE. |

### pattern

Desired layout pattern. Use DSLayoutPatternUnknown for auto-detection.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) DSLayoutPattern pattern;
```
2. 
```swift
var pattern: LayoutPattern { get set }
```

### axes

Configuration for primary axis [0] and secondary axis [1].

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong) NSArray<DSLayoutAxis *> *axes;
```
2. 
```swift
var axes: [LayoutAxis] { get set }
```

### inputImageWidth

Width of the reference image. Required when spacingUnit is MU_PERCENTAGE.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger inputImageWidth;
```
2. 
```swift
var inputImageWidth: Int { get set }
```

### inputImageHeight

Height of the reference image. Required when spacingUnit is MU_PERCENTAGE.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger inputImageHeight;
```
2. 
```swift
var inputImageHeight: Int { get set }
```
