---
layout: default-layout
Title: DSMultiFrameResultCrossFilter - Dynamsoft Capture Vision Router Module iOS Edition API Reference
Description: The class DSMultiFrameResultCrossFilter of Dynamsoft Capture Vision Router Module is responsible for filtering captured results.
Keywords: multi-frame result cross filter, objective-c, swift
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
| [`enableResultDeduplication`](#enableresultdeduplication) | Enable duplicate filter feature to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition. |
| [`enableResultCrossVerification`](#enableresultcrossverification) | Enable result verification feature to improve the accuracy of video streaming recognition results. |
| [`setDuplicateForgetTime`](#setduplicateforgettime) | Sets the duplicate forget time for the specific captured result item types. |
| [`isResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Whether the duplicate filter feature is enabled for the specific result item type. |
| [`isResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Whether the result verification feature is enabled for the specific result item type. |
| [`getDuplicateForgetTime`](#getduplicateforgettime) | Gets the duplicate forget time for the specific captured result item types. |

### enableResultDeduplication

Enable duplicate filter feature to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition.

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

`resultItemType`: Specifies a targeting captured result type.

`isEnabled`: A BOOL value that indicates whether to enable the duplicate filter feature.

### enableResultCrossVerification

Enable result verification feature to improve the accuracy of video streaming recognition results.

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

`resultItemType`: Specifies a targeting captured result type.

`isEnabled`: A BOOL value that indicates whether to enable the result verification feature.

### setDuplicateForgetTime

Sets the duplicate forget time for the specific captured result item types.

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

`resultItemType`: Specifies a targeting captured result type.

`duplicateForgetTime`: The duplicate forget time of the specified capture result type.

### isResultDeduplicationEnabled

Whether the duplicate filter feature is enabled for the specific result item type.

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

`resultItemType`: Specifies a targeting captured result type.

**Return Value**

A BOOL value that indicates whether the duplicate filter feature is enabled for the specific result item type.

### isResultCrossVerificationEnabled

Whether the result verification feature is enabled for the specific result item type.

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

`resultItemType`: Specifies a targeting captured result type.

**Return Value**

A BOOL value that indicates whether the result verification feature is enabled for the specific result item type.

### getDuplicateForgetTime

Gets the duplicate forget time for the specific captured result item types.

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

`resultItemType`: Specifies a targeting captured result type.

**Return Value**

The duplicate forget time of the specified capture result type.
