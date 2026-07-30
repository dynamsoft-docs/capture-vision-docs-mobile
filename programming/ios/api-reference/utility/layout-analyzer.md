---
layout: default-layout
title: DSLayoutAnalyzer - Dynamsoft Capture Vision iOS Edition API Reference
description: The class DSLayoutAnalyzer of Dynamsoft Capture Vision iOS edition provides quadrilateral layout analysis functionality.
keywords: layout analyzer, quadrilateral, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSLayoutAnalyzer

The `DSLayoutAnalyzer` class provides static methods to analyze the spatial distribution of quadrilaterals.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
NS_SWIFT_NAME(LayoutAnalyzer)
@interface DSLayoutAnalyzer : NSObject
```
2. 
```swift
class LayoutAnalyzer : NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`analyze(inputQuads:)`](#analyzeinputquads) | Analyzes the spatial distribution of quadrilaterals. |
| [`analyze(inputQuads:parameter:)`](#analyzeinputquadsparameter) | Analyzes the spatial distribution of quadrilaterals with optional constraints. |

### analyze(inputQuads:)

Analyzes the spatial distribution of quadrilaterals.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+ (nullable DSLayoutAnalysisResult *)analyze:(NSArray<DSQuadrilateral *> *)inputQuads;
```
2. 
```swift
class func analyze(_ inputQuads: [Quadrilateral]) -> LayoutAnalysisResult?
```

**Parameters**

`inputQuads`: Array of input quadrilaterals.

**Return Value**

A [`DSLayoutAnalysisResult`](layout-analysis-result.md) object, or nil on failure.

### analyze(inputQuads:parameter:)

Analyzes the spatial distribution of quadrilaterals with optional constraints.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+ (nullable DSLayoutAnalysisResult *)analyze:(NSArray<DSQuadrilateral *> *)inputQuads
                  parameter:(nullable DSLayoutAnalysisParameter *)parameter;
```
2. 
```swift
class func analyze(_ inputQuads: [Quadrilateral], parameter: LayoutAnalysisParameter?) -> LayoutAnalysisResult?
```

**Parameters**

`inputQuads`: Array of input quadrilaterals.

`parameter`: Optional parameters to constrain the analysis.

**Return Value**

A [`DSLayoutAnalysisResult`](layout-analysis-result.md) object, or nil on failure.
