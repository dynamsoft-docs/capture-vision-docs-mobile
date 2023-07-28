---
layout: default-layout
Title: MultiFrameResultCrossFilter - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The class MultiFrameResultCrossFilter of Dynamsoft Capture Vision Router Module is responsible for filtering captured results.
Keywords: multi-frame result cross filter, Java, Kotlin
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
| [`enableResultDeduplication`](#enableresultdeduplication) | Enable duplicate filter feature to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition. |
| [`enableResultCrossVerification`](#enableresultcrossverification) | Enable result verification feature to improve the accuracy of video streaming recognition results. |
| [`setDuplicateForgetTime`](#setduplicateforgettime) | Sets the duplicate forget time for the specific captured result item types. |
| [`isResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Whether the duplicate filter feature is enabled for the specific result item type. |
| [`isResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Whether the result verification feature is enabled for the specific result item type. |
| [`getDuplicateForgetTime`](#getduplicateforgettime) | Gets the duplicate forget time for the specific captured result item types. |

### enableResultDeduplication

Enable result deduplication to filter out the duplicate results in the period of duplicateForgetTime for video streaming recognition.

```java
void enableResultDeduplication(int resultItemTypes, bool enable);
```

**Parameters**

`[in] resultItemTypes`: Specifies a targeting captured result type.  

`[in] enable`: A boolean value that indicates whether to enable the duplicate filter feature.

### enableResultCrossVerification

Enable result cross verification feature to improve the accuracy of video streaming recognition results.

```java
void enableResultCrossVerification(int resultItemTypes, bool enable);
```

**Parameters**

`[in] resultItemTypes`: Specifies a targeting captured result type.  

`[in] enable`: A boolean value that indicates whether to enable the result verification feature.

### setDuplicateForgetTime

Sets the duplicate forget time for the specific captured result item types.

```java
void setDuplicateForgetTime(int resultItemTypes, int time);
```

**Parameters**

`[in] resultItemType`: Specifies a targeting captured result type.  

`[in] time`: The duplicate forget time of the specified capture result type.

### isResultDeduplicationEnabled

Whether the result deduplication feature is enabled for the specific result item type.

```java
boolean isResultDeduplicationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type`: Specifies a targeting captured result type.

**Return Value**

A boolean value that indicates whether the duplicate filter feature is enabled for the specific result item type.

### isResultCrossVerificationEnabled

Whether the result verification feature is enabled for the specific result item type.

```java
boolean isResultCrossVerificationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type`: Specifies a targeting captured result type.

**Return Value**

A boolean value that indicates whether the result verification feature is enabled for the specific result item type.

### getDuplicateForgetTime

Gets the duplicate forget time for the specific captured result item types.

```java
int getDuplicateForgetTime(CapturedResultItemType type);
```

**Parameters**

`[in] type`: Specifies a targeting captured result type.

**Return Value**

The duplicate forget time of the specified capture result type.
