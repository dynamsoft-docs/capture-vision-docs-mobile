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

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class MultiFrameResultCrossFilter implements CapturedResultFilter
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

```java
void enableLatestOverlapping(@EnumCapturedResultItemType int type, boolean enable);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

`[in] enable`: Boolean to toggle to-the-latest overlapping on or off.

### enableResultCrossVerification

Enables or disables the verification of one or multiple specific result item types.

```java
void enableResultCrossVerification(@EnumCapturedResultItemType int resultItemTypes, bool enable);
```

**Parameters**

`[in] type`: Specifies one or multiple specific result item types, which can be defined using [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

`[in] enable`: Boolean to toggle verification on or off.

### enableResultDeduplication

Enables or disables the deduplication process for one or multiple specific result item types.

```java
void enableResultDeduplication(@EnumCapturedResultItemType int resultItemTypes, bool enable);
```

**Parameters**

`[in] type`: Specifies one or multiple specific result item types, which can be defined using [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

`[in] enable`: Boolean to toggle deduplication on or off.

### getDuplicateForgetTime

Gets the interval during which duplicates are disregarded for a given result item type.

```java
int getDuplicateForgetTime(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

**Return Value**

The set interval for the specified item type.

### getMaxOverlappingFrames

Get the maximum overlapping frames count for a given result item type.

```java
int getMaxOverlappingFrames(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

**Return Value**

The maximum overlapping frame count for the overlapping.

### isLatestOverlappingEnabled

Checks if to-the-latest overlapping is active for a given result item type.

```java
boolean isLatestOverlappingEnabled(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

**Return Value**

Boolean indicating the to-the-latest overlapping status for the specified type.

### isResultDeduplicationEnabled

Checks if deduplication is active for a given result item type.

```java
boolean isResultDeduplicationEnabled(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

**Return Value**

Boolean indicating the deduplication status for the specified type.

### isResultCrossVerificationEnabled

Checks if verification is active for a given result item type.

```java
boolean isResultCrossVerificationEnabled(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

**Return Value**

Boolean indicating the status of verification for the specified type.

### setDuplicateForgetTime

Sets the interval during which duplicates are disregarded for a given result item type.

```java
void setDuplicateForgetTime(@EnumCapturedResultItemType int resultItemTypes, int time);
```

**Parameters**

`[in] type`: Specifies one or multiple specific result item types, which can be defined using [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

`[in] time`: Time in milliseconds during which duplicates are disregarded.

### setMaxOverlappingFrames

Set the maximum overlapping frames count for a given result item type. You can set it higher if:

- You capture device is stationary or moving stably.
- You want to further improve the read-rate.

```java
void setMaxOverlappingFrames(@EnumCapturedResultItemType int type, int maxOverlappingFrames);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_enumerations }}core/captured-result-item-type.html?lang=android).

`[in] maxOverlappingFrames`: The maximum overlapping frame count for the overlapping.
