---
layout: default-layout
title: MultiFrameResultCrossFilter - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class MultiFrameResultCrossFilter of Dynamsoft Capture Vision Router Module is responsible for filtering captured results.
keywords: multi-frame result cross filter, Filter
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
class MultiFrameResultCrossFilter implements CapturedResultFilter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`enableResultDeduplication`](#enableresultdeduplication) | Enables or disables the deduplication process for one or multiple specific result item types. |
| [`enableResultCrossVerification`](#enableresultcrossverification) | Enables or disables the verification of one or multiple specific result item types. |
| [`setDuplicateForgetTime`](#setduplicateforgettime) | Sets the interval during which duplicates are disregarded for a given result item type. |
| [`isResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Checks if deduplication is active for a given result item type. |
| [`isResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Checks if verification is active for a given result item type. |
| [`getDuplicateForgetTime`](#getduplicateforgettime) | Gets the interval during which duplicates are disregarded for a given result item type. |

### enableResultDeduplication

Enables or disables the deduplication process for one or multiple specific result item types.

```java
void enableResultDeduplication(int resultItemTypes, bool enable);
```

**Parameters**

`[in] type`: Specifies one or multiple specific result item types, which can be defined using [`CapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

`[in] enable`: Boolean to toggle deduplication on or off.

### enableResultCrossVerification

Enables or disables the verification of one or multiple specific result item types.

```java
void enableResultCrossVerification(int resultItemTypes, bool enable);
```

**Parameters**

`[in] type`: Specifies one or multiple specific result item types, which can be defined using [`CapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

`[in] enable`: Boolean to toggle verification on or off.

### setDuplicateForgetTime

Sets the interval during which duplicates are disregarded for a given result item type.

```java
void setDuplicateForgetTime(int resultItemTypes, int time);
```

**Parameters**

`[in] type`: Specifies one or multiple specific result item types, which can be defined using [`CapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

`[in] time`: Time in milliseconds during which duplicates are disregarded.

### isResultDeduplicationEnabled

Checks if deduplication is active for a given result item type.

```java
boolean isResultDeduplicationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`CapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

**Return Value**

Boolean indicating the deduplication status for the specified type.

### isResultCrossVerificationEnabled

Checks if verification is active for a given result item type.

```java
boolean isResultCrossVerificationEnabled(CapturedResultItemType type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`CapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

**Return Value**

Boolean indicating the status of verification for the specified type.

### getDuplicateForgetTime

Gets the interval during which duplicates are disregarded for a given result item type.

```java
int getDuplicateForgetTime(CapturedResultItemType type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`CapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

**Return Value**

The set interval for the specified item type.
