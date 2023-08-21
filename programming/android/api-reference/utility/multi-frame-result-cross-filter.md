---
layout: default-layout
Title: MultiFrameResultCrossFilter - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The class MultiFrameResultCrossFilter of Dynamsoft Capture Vision Router Module is responsible for filtering captured results.
Keywords: multi-frame result cross filter, Filter
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# MultiFrameResultCrossFilter

The `MultiFrameResultCrossFilter` class is responsible for filtering captured results.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftUtility.aar

```java
class MultiFrameResultCrossFilter
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

```java
void enableResultDeduplication(int resultItemTypes, bool enable);
```

**Parameters**

`[in] resultItemTypes`: Specifies a targeting captured result type.  

`[in] enable`: A boolean value that indicates whether to enable the result deduplication feature.

### enableResultCrossVerification

Enable result cross verification to improve the accuracy of video streaming recognition results.

```java
void enableResultCrossVerification(int resultItemTypes, bool enable);
```

**Parameters**

`[in] resultItemTypes`: Specifies a targeting captured result type.  

`[in] enable`: A boolean value that indicates whether to enable the result cross verification feature.

### setDuplicateForgetTime

Sets the time period during which duplicate results of the specified result type are discarded.

```java
void setDuplicateForgetTime(int resultItemTypes, int time);
```

**Parameters**

`[in] resultItemType`: Specifies a targeting captured result type.  

`[in] time`: The duplicate forget time of the specified capture result type.

### isResultDeduplicationEnabled

Returns whether the result cross verification feature is enabled for the specified result item type.

```java
boolean isResultDeduplicationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type`: Specifies a targeting captured result type.

**Return Value**

A boolean value that indicates whether the result deduplication feature is enabled for the specific result item type.

### isResultCrossVerificationEnabled

Returns whether the result cross verification feature is enabled for the specified result item type.

```java
boolean isResultCrossVerificationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type`: Specifies a targeting captured result type.

**Return Value**

A boolean value that indicates whether the result cross verification feature is enabled for the specific result item type.

### getDuplicateForgetTime

Gets the time period during which duplicate results of the specified  result type.

```java
int getDuplicateForgetTime(CapturedResultItemType type);
```

**Parameters**

`[in] type`: Specifies a targeting captured result type.

**Return Value**

The duplicate forget time of the specified capture result type.
