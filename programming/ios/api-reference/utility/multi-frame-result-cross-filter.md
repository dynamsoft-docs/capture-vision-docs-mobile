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

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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
| [`enableLatestOverlapping`](#enablelatestoverlapping) | Enables or disables the to-the-latest overlapping feature of one or multiple specific result item types. This feature can sharpenly increase the read-rate performance when decoding multiple barcodes under the video streaming. |
| [`enableResultCrossVerification`](#enableresultcrossverification) | Enables or disables the verification of one or multiple specific result item types. |
| [`enableResultDeduplication`](#enableresultdeduplication) | Enables or disables the deduplication process for one or multiple specific result item types. |
| [`getDuplicateForgetTime`](#getduplicateforgettime) | Gets the interval during which duplicates are disregarded for a given result item type. |
| [`getMaxOverlappingFrames`](#getmaxoverlappingframes) | Get the maximum overlapping frames count for a given result item type. |
| [`isLatestOverlappingEnabled`](#islatestoverlappingenabled) | Checks if to-the-latest overlapping is active for a given result item type. |
| [`isResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Checks if verification is active for a given result item type. |
| [`isResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Checks if deduplication is active for a given result item type. |
| [`setDuplicateForgetTime`](#setduplicateforgettime) | Sets the interval during which duplicates are disregarded for specific result item types. |
| [`setMaxOverlappingFrames`](#setmaxoverlappingframes) | Set the maximum overlapping frames count for a given result item type. |

### enableLatestOverlapping

Enables or disables the to-the-latest overlapping feature of one or multiple specific result item types. This feature can sharpenly increase the read-rate performance when decoding multiple barcodes under the video streaming.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)enableLatestOverlapping:(DSCapturedResultItemType)resultItemTypes
                      isEnabled:(BOOL)isEnabled;
```
2. 
```swift
func enableLatestOverlapping(resultItemTypes: DSCapturedResultItemType, isEnabled: Bool)
```

**Parameters**

`[in] type`: Specifies the result item type with [`DSCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

`[in] enable`: Bool to toggle to-the-latest overlapping on or off.

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

`resultItemType`: Specifies one or multiple specific result item types, which can be defined using [`DSCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

`isEnabled`: A BOOL value that indicates whether to enable the result cross verification feature.

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

`resultItemType`: Specifies one or multiple specific result item types, which can be defined using [`DSCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

`isEnabled`: A BOOL value that indicates whether to enable the result deduplication feature.

### getDuplicateForgetTime

Gets the interval during which duplicates are disregarded for a given result item type.

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

`resultItemType`: Specifies the result item type with [`DSCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

**Return Value**

The set interval for the specified item type.

### getMaxOverlappingFrames

Get the maximum overlapping frames count for a given result item type.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)getMaxOverlappingFrames:(DSCapturedResultItemType)resultItemType;
```
2. 
```swift
func getMaxOverlappingFrames(resultItemType: DSCapturedResultItemType) -> Int
```

**Parameters**

`[in] type`: Specifies the result item type with [`DSCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

**Return Value**

The maximum overlapping frame count for the overlapping.

### isLatestOverlappingEnabled

Checks if to-the-latest overlapping is active for a given result item type.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)isLatestOverlappingEnabled:(DSCapturedResultItemType)resultItemTypes;
```
2. 
```swift
func isLatestOverlappingEnabled(resultItemType: DSCapturedResultItemType) -> Bool
```

**Parameters**

`[in] type`: Specifies the result item type with [`DSCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

**Return Value**

Boolean indicating the to-the-latest overlapping status for the specified type.

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

`resultItemType`: Specifies the result item type with [`DSCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

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

`resultItemType`: Specifies the result item type with [`DSCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

**Return Value**

Boolean indicating the status of verification for the specified type.

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

`resultItemType`: Specifies one or multiple specific result item types, which can be defined using [`DSCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

`duplicateForgetTime`: The duplicate forget time of the specified capture result type.

### setMaxOverlappingFrames

Set the maximum overlapping frames count for a given result item type.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)setMaxOverlappingFrames:(DSCapturedResultItemType)resultItemTypes
           maxOverlappingFrames:(NSInteger)maxOverlappingFrames;
```
2. 
```swift
func setMaxOverlappingFrames(resultItemType: DSCapturedResultItemType, maxOverlappingFrames: Int)
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_ios_api }}core/enum/captured-result-item-type.html?lang=objc,swift).

`[in] maxOverlappingFrames`: The maximum overlapping frame count for the overlapping.
