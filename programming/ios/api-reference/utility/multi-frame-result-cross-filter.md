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
| [`enableResultDeduplication`](#enableresultdeduplication) | Enable filtering out duplicate consecutive results in the period set by `setDuplicateForgetTime` for video streaming recognition. |
| [`enableResultCrossVerification`](#enableresultcrossverification) | Enable result cross verification to improve the accuracy of video streaming recognition results. |
| [`setDuplicateForgetTime`](#setduplicateforgettime) | Sets the time period during which duplicate results of the specified result type are discarded. |
| [`isResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Returns whether the result deduplication feature is enabled for the specified result item type. |
| [`isResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Returns whether the result cross verification feature is enabled for the specified result item type. |
| [`getDuplicateForgetTime`](#getduplicateforgettime) | Gets the time period during which duplicate results of the specified  result type. |

### enableResultDeduplication

Enable filtering out duplicate consecutive results in the period set by `setDuplicateForgetTime` for video streaming recognition.

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

`isEnabled`: A BOOL value that indicates whether to enable the result deduplication feature.

### enableResultCrossVerification

Enable result cross verification feature to improve the accuracy of video streaming recognition results.

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

`isEnabled`: A BOOL value that indicates whether to enable the result cross verification feature.

### setDuplicateForgetTime

Sets the time period during which duplicate results of the specified result type are discarded.

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

Returns whether the result deduplication feature is enabled for the specified result item type.

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

A BOOL value that indicates whether the result deduplication feature is enabled for the specific result item type.

### isResultCrossVerificationEnabled

Returns whether the result cross verification feature is enabled for the specified result item type.

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

A BOOL value that indicates whether the result cross verification feature is enabled for the specific result item type.

### getDuplicateForgetTime

Gets the time period during which duplicate results of the specified  result type.

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
