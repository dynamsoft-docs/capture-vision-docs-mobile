---
layout: default-layout
title: DSLayoutAnalysisResult - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSLayoutAnalysisResult of Dynamsoft Capture Vision iOS edition represents the results of a layout analysis.
keywords: layout analysis result, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLayoutAnalysisResult

The `DSLayoutAnalysisResult` class represents the comprehensive results of the layout analysis.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(LayoutAnalysisResult)
@interface DSLayoutAnalysisResult : NSObject
```
2. 
```swift
class LayoutAnalysisResult : NSObject
```

## Attributes

| Attribute | Type | Description |
| --------- | ---- | ----------- |
| [`inferredQuads`](#inferredquads) | *NSArray<DSQuadrilateral \*> \** | Array of newly generated quadrilaterals. |
| [`elements`](#elements) | *NSArray<NSArray<DSLayoutElement \*> \*> \** | A 2D array of layout elements [rowCount][colCount]. |
| [`rowCount`](#rowcount) | *NSInteger* | Number of rows in the analyzed layout. |
| [`colCount`](#colcount) | *NSInteger* | Maximum number of columns across all rows. |
| [`detectedPattern`](#detectedpattern) | *DSLayoutPattern* | The actual layout pattern identified by the engine. |
| [`errorCode`](#errorcode) | *NSInteger* | 0 for success, non-zero for error. |

### inferredQuads

Array of newly generated quadrilaterals.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong) NSArray<DSQuadrilateral *> *inferredQuads;
```
2. 
```swift
var inferredQuads: [Quadrilateral] { get set }
```

### elements

A 2D array of layout elements [rowCount][colCount].

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong) NSArray<NSArray<DSLayoutElement *> *> *elements;
```
2. 
```swift
var elements: [[LayoutElement]] { get set }
```

### rowCount

Number of rows in the analyzed layout.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger rowCount;
```
2. 
```swift
var rowCount: Int { get set }
```

### colCount

Maximum number of columns across all rows.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger colCount;
```
2. 
```swift
var colCount: Int { get set }
```

### detectedPattern

The actual layout pattern identified by the engine.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) DSLayoutPattern detectedPattern;
```
2. 
```swift
var detectedPattern: LayoutPattern { get set }
```

### errorCode

0 for success, non-zero for error.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger errorCode;
```
2. 
```swift
var errorCode: Int { get set }
```
