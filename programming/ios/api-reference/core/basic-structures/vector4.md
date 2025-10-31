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

## Attributes & Methods

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`value`](#value) | *NSArray* | The components value of a four-dimensional vector. |

| Method | Description |
| ------ | ----------- |
| [`initWithIntegerValue`](#initwithintegervalue) | The constructor. Creates a DSVector4 from the specified parameters. |

### value

The components value of a four-dimensional vector.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, copy, readonly) NSArray *values;
```
2. 
```swift
var value: [Int] { get }
```

### initWithIntegerValue

The constructor. Creates a DSVector4 from the specified parameters.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)initWithIntegerValue:(NSInteger)v1
                                  v2:(NSInteger)v2
                                  v3:(NSInteger)v3
                                  v4:(NSInteger)v4;
```
2. 
```swift
init(v1: Int, v2: Int, v3: Int, v4: Int)
```
