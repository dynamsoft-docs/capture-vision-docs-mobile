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
| [`enableDuplicateFilter`](#enableduplicatefilter) | Enable duplicate filter feature to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition. |
| [`enableResultVerification`](#enableresultverification) | Enable result verification feature to improve the accuracy of video streaming recognition results. |
| [`setDuplicateForgetTime`](#setduplicateforgettime) | Sets the duplicate forget time for the specific captured result item types. |
| [`isDuplicateFilterEnabled`](#isduplicatefilterenabled) | Whether the duplicate filter feature is enabled for the specific result item type. |
| [`isResultVerificationEnabled`](#isresultverificationenabled) | Whether the result verification feature is enabled for the specific result item type. |
| [`getDuplicateForgetTime`](#getduplicateforgettime) | Gets the duplicate forget time for the specific captured result item types. |
| [`onRawImageResultReceived`](#onrawimageresultreceived) | Callback method for receiving raw image result items. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | Callback method for receiving decoded barcode results. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | Callback method for receiving recognized text line results. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | Callback method for receiving detected quad results. |
| [`onNormalizedImagesReceived`](#onnormalizedimagesreceived) | Callback method for receiving normalized image results. |
| [`onParsedResultsReceived`](#onparsedresultsreceived) | Callback method for receiving parsed results. |

### enableDuplicateFilter

Enable duplicate filter feature to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)enableDuplicateFilter:(DSCapturedResultItemType)resultItemType
                    isEnabled:(BOOL)isEnabled;
```
2. 
```swift
func enableDuplicateFilter(resultItemType: DSCapturedResultItemType, isEnabled: Bool)
```

**Parameters**

`resultItemType`: Specifies a targeting captured result type.

`isEnabled`: A BOOL value that indicates whether to enable the duplicate filter feature.

### enableResultVerification

Enable result verification feature to improve the accuracy of video streaming recognition results.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)enableResultVerification:(DSCapturedResultItemType)resultItemType
                    isEnabled:(BOOL)isEnabled;
```
2. 
```swift
func enableResultVerification(resultItemType: DSCapturedResultItemType, isEnabled: Bool)
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

### isDuplicateFilterEnabled

Whether the duplicate filter feature is enabled for the specific result item type.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (bool)isDuplicateFilterEnabled:(DSCapturedResultItemType)resultItemType;
```
2. 
```swift
func isDuplicateFilterEnabled(resultItemType: DSCapturedResultItemType) -> Bool
```

**Parameters**

`resultItemType`: Specifies a targeting captured result type.

**Return Value**

A BOOL value that indicates whether the duplicate filter feature is enabled for the specific result item type.

### isResultVerificationEnabled

Whether the result verification feature is enabled for the specific result item type.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (bool)isResultVerificationEnabled:(DSCapturedResultItemType)resultItemType;
```
2. 
```swift
func isResultVerificationEnabled(resultItemType: DSCapturedResultItemType) -> Bool
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

### onRawImageResultReceived

Callback method for receiving raw image result items.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onRawImageResultReceived:(DSRawImageResultItem *)pResult;
```
2. 
```swift
func onRawImageResultReceived(pResult: DSRawImageResultItem)
```

**Parameters**

`pResult`: A `DSRawImageResultItem` object representing the raw image result.

### onDecodedBarcodesReceived

Callback method for receiving decoded barcode results.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onDecodedBarcodesReceived:(DSDecodedBarcodesResult *)pResult;
```
2. 
```swift
func onDecodedBarcodesReceived(pResult: DSDecodedBarcodesResult)
```

**Parameters**

`pResult`: A `DSDecodedBarcodesResult` object representing the decoded barcode result.

### onRecognizedTextLinesReceived

Callback method for receiving recognized text line results.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onRecognizedTextLinesReceived:(DSRecognizedTextLinesResult *)pResult;
```
2. 
```swift
func onRecognizedTextLinesReceived(pResult: DSRecognizedTextLinesResult)
```

**Parameters**

`pResult`: A `DSRecognizedTextLinesResult` object representing the recognized text line result.

### onDetectedQuadsReceived

Callback method for receiving detected quad results.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onDetectedQuadsReceived:(DSDetectedQuadsResult *)pResult;
```
2. 
```swift
func onDetectedQuadsReceived(pResult: DSDetectedQuadsResult)
```

**Parameters**

`pResult`: A `DSDetectedQuadsResult` object representing the detected quad result.

### onNormalizedImagesReceived

Callback method for receiving normalized image results.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onNormalizedImagesReceived:(DSNormalizedImagesResult *)pResult;
```
2. 
```swift
func onNormalizedImagesReceived(pResult: DSNormalizedImagesResult)
```

**Parameters**

`pResult`: A `DSNormalizedImagesResult` object representing the normalized image result.

### onParsedResultsReceived

Callback method for receiving parsed results.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onParsedResultsReceived:(DSParsedResult *)pResult;
```
2. 
```swift
func onParsedResultsReceived(pResult: DSParsedResult)
```

**Parameters**

`pResult`: A `DSParsedResult` object representing the parsed result.

