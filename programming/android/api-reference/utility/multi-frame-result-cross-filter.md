---
layout: default-layout
Title: DSMultiFrameResultCrossFilter - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The class DSMultiFrameResultCrossFilter of Dynamsoft Capture Vision Router Module is responsible for filtering captured results.
Keywords: multi-frame result cross filter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSMultiFrameResultCrossFilter

The `DSMultiFrameResultCrossFilter` class is responsible for filtering captured results.

## Definition

*Namespace*: com.dynamsoft.utility  
*Assembly:* DynamsoftUtility.aar

```java
class MultiFrameResultCrossFilter, CapturedResultFilter
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

### enableDuplicateFilter

Enable duplicate filter feature to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition.

```java
func enableDuplicateFilter(resultItemType: CapturedResultItemType, isEnabled: Bool)
```

**Parameters**

`resultItemType`: Specifies a targeting captured result type.  
`isEnabled`: A BOOL value that indicates whether to enable the duplicate filter feature.

### enableResultVerification

Enable result verification feature to improve the accuracy of video streaming recognition results.

```java
func enableResultVerification(resultItemType: CapturedResultItemType, isEnabled: Bool)
```

**Parameters**

`resultItemType`: Specifies a targeting captured result type.  
`isEnabled`: A BOOL value that indicates whether to enable the result verification feature.

### setDuplicateForgetTime

Sets the duplicate forget time for the specific captured result item types.

```java
func setDuplicateForgetTime(resultItemType: CapturedResultItemType, duplicateForgetTime: Int)
```

**Parameters**

`resultItemType`: Specifies a targeting captured result type.  
`duplicateForgetTime`: The duplicate forget time of the specified capture result type.

### isDuplicateFilterEnabled

Whether the duplicate filter feature is enabled for the specific result item type.

```java
func isDuplicateFilterEnabled(resultItemType: CapturedResultItemType) -> Bool
```

**Parameters**

`resultItemType`: Specifies a targeting captured result type.

**Return Value**

A BOOL value that indicates whether the duplicate filter feature is enabled for the specific result item type.

### isResultVerificationEnabled

Whether the result verification feature is enabled for the specific result item type.

```java
func isResultVerificationEnabled(resultItemType: CapturedResultItemType) -> Bool
```

**Parameters**

`resultItemType`: Specifies a targeting captured result type.

**Return Value**

A BOOL value that indicates whether the result verification feature is enabled for the specific result item type.

### getDuplicateForgetTime

Gets the duplicate forget time for the specific captured result item types.

```java
func getDuplicateForgetTime(resultItemType: CapturedResultItemType) -> Int
```

**Parameters**

`resultItemType`: Specifies a targeting captured result type.

**Return Value**

The duplicate forget time of the specified capture result type.
