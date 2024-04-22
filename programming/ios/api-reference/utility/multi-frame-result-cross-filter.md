---
layout: default-layout
title: DSMultiFrameResultCrossFilter - Dynamsoft Capture Vision Router Module iOS Edition API Reference
description: The class DSMultiFrameResultCrossFilter of Dynamsoft Capture Vision Router Module is responsible for filtering captured results.
keywords: multi-frame result cross filter, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSMultiFrameResultCrossFilter

The `DSMultiFrameResultCrossFilter` class is responsible for filtering captured results.

## Definition

*Assembly:* DynamsoftUtility.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSMultiFrameResultCrossFilter ()<CapturedResultFilter>
```
2. 
```swift
class MultiFrameResultCrossFilter: NSObject, CapturedResultFilter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`enableResultDeduplication`](#enableresultdeduplication) | Enables or disables the deduplication process for one or multiple specific result item types. |
| [`enableResultCrossVerification`](#enableresultcrossverification) | Enables or disables the verification of one or multiple specific result item types. |
| [`setDuplicateForgetTime`](#setduplicateforgettime) | Sets the interval during which duplicates are disregarded for specific result item types. |
| [`isResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Checks if deduplication is active for a given result item type. |
| [`isResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Checks if verification is active for a given result item type. |
| [`getDuplicateForgetTime`](#getduplicateforgettime) | Gets the interval during which duplicates are disregarded for specific result item types. |

### enableResultDeduplication

Enables or disables the deduplication process for one or multiple specific result item types.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)enableResultDeduplication:(DSCapturedResultItemType)resultItemType
                        isEnabled:(BOOL)isEnabled;
```
2. 
```swift
func enableResultDeduplication(resultItemType: DSCapturedResultItemType, isEnabled: Bool)
```

**Parameters**

`resultItemType`: Specifies one or multiple specific result item types, which can be defined using [`DSCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=objc,swift).

`isEnabled`: A BOOL value that indicates whether to enable the result deduplication feature.

### enableResultCrossVerification

Enables or disables the verification of one or multiple specific result item types.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)enableResultCrossVerification:(DSCapturedResultItemType)resultItemType
                    isEnabled:(BOOL)isEnabled;
```
2. 
```swift
func enableResultCrossVerification(resultItemType: DSCapturedResultItemType, isEnabled: Bool)
```

**Parameters**

`resultItemType`: Specifies one or multiple specific result item types, which can be defined using [`DSCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=objc,swift).

`isEnabled`: A BOOL value that indicates whether to enable the result cross verification feature.

### setDuplicateForgetTime

Sets the interval during which duplicates are disregarded for specific result item types.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)setDuplicateForgetTime:(DSCapturedResultItemType)resultItemType
            duplicateForgetTime:(NSInteger)duplicateForgetTime;
```
2. 
```swift
func setDuplicateForgetTime(resultItemType: DSCapturedResultItemType, duplicateForgetTime: Int)
```

**Parameters**

`resultItemType`: Specifies one or multiple specific result item types, which can be defined using [`DSCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=objc,swift).

`duplicateForgetTime`: The duplicate forget time of the specified capture result type.

### isResultDeduplicationEnabled

Checks if deduplication is active for a given result item type.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (bool)isResultDeduplicationEnabled:(DSCapturedResultItemType)resultItemType;
```
2. 
```swift
func isResultDeduplicationEnabled(resultItemType: DSCapturedResultItemType) -> Bool
```

**Parameters**

`resultItemType`: Specifies the result item type with [`DSCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=objc,swift).

**Return Value**

Boolean indicating the deduplication status for the specified type.

### isResultCrossVerificationEnabled

Checks if verification is active for a given result item type.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (bool)isResultCrossVerificationEnabled:(DSCapturedResultItemType)resultItemType;
```
2. 
```swift
func isResultCrossVerificationEnabled(resultItemType: DSCapturedResultItemType) -> Bool
```

**Parameters**

`resultItemType`: Specifies the result item type with [`DSCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=objc,swift).

**Return Value**

Boolean indicating the status of verification for the specified type.

### getDuplicateForgetTime

Gets the interval during which duplicates are disregarded for specific result item types.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)getDuplicateForgetTime:(DSCapturedResultItemType)resultItemType;
```
2. 
```swift
func getDuplicateForgetTime(resultItemType: DSCapturedResultItemType) -> Int
```

**Parameters**

`resultItemType`: Specifies the result item type with [`DSCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=objc,swift).

**Return Value**

The set interval for the specified item type.
