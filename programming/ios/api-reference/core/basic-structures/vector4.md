---
layout: default-layout
title: DSVector4 - Dynamsoft Core Module iOS Edition API Reference
description: The class DSVector4 of Dynamsoft Core Module represents a a four-dimensional vector.
keywords: vector4, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSVector4

The `DSVector4` class represents a four-dimensional vector.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSVector4 : NSObject
```
2. 
```swift
class Vector4 : NSObject
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`value`](#value) | *NSArray* | The components value of a four-dimensional vector. |

### value

The components value of a four-dimensional vector.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, copy) NSArray *value;
```
2. 
```swift
var value: [Int] { get set }
```
