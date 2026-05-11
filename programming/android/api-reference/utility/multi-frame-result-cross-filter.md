---
layout: default-layout
title: MultiFrameResultCrossFilter - Dynamsoft Capture Vision Android Edition API Reference
description: The class MultiFrameResultCrossFilter of Dynamsoft Capture Vision Android is responsible for filtering captured results.
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
| [`MultiFrameResultCrossFilter`](#multiframeresultcrossfilter-1) | The constructor. |
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
| [`setResultCrossVerificationCriteria`](#setresultcrossverificationcriteria) | Sets the cross-verification criteria for specified result item types. |
| [`getResultCrossVerificationCriteria`](#getresultcrossverificationcriteria) | Gets the cross-verification criteria for a specified result item type. |

### MultiFrameResultCrossFilter

The constructor.

```java
MultiFrameResultCrossFilter();
```

### enableResultCrossVerification

Enables or disables the verification of one or multiple specific result item types.

```java
void enableResultCrossVerification(@EnumCapturedResultItemType int resultItemTypes, boolean enable);
```

**Parameters**

`[in] type`: Specifies one or multiple specific result item types, which can be defined using [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

`[in] enable`: Boolean to toggle verification on or off.

> [!Note]
> 
> The verification is enabled by default for `CRIT_TEXT_LINE` & `CRIT_DETECTED_QUAD` type result items.

### isResultCrossVerificationEnabled

Checks if verification is active for a given result item type.

```java
boolean isResultCrossVerificationEnabled(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

**Return Value**

Boolean indicating the status of verification for the specified type.

### enableResultDeduplication

Enables or disables the deduplication process for one or multiple specific result item types.

```java
void enableResultDeduplication(@EnumCapturedResultItemType int resultItemTypes, boolean enable);
```

**Parameters**

`[in] type`: Specifies one or multiple specific result item types, which can be defined using [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

`[in] enable`: Boolean to toggle deduplication on or off.

**Remarks**

Result deduplication is disabled by default. You can enable it and adjust the `DuplicateForgetTime` based on your requirements.

### isResultDeduplicationEnabled

Checks if deduplication is active for a given result item type.

```java
boolean isResultDeduplicationEnabled(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

**Return Value**

Boolean indicating the deduplication status for the specified type.

### setDuplicateForgetTime

Sets the interval during which duplicates are disregarded for a given result item type.

```java
void setDuplicateForgetTime(@EnumCapturedResultItemType int resultItemTypes, int time);
```

**Parameters**

`[in] type`: Specifies one or multiple specific result item types, which can be defined using [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

`[in] time`: Time in milliseconds during which duplicates are disregarded.

**Remarks**

The default value is 3,000 milliseconds. This means that when result deduplication is enabled, identical results appearing within 3 seconds of each other will be filtered out by default. The maximum allowed value is 180,000 milliseconds.

### getDuplicateForgetTime

Gets the interval during which duplicates are disregarded for a given result item type.

```java
int getDuplicateForgetTime(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

**Return Value**

The set interval for the specified item type.

### enableLatestOverlapping

Enables or disables the to-the-latest overlapping feature of one or multiple specific result item types. This feature can sharpenly increase the read-rate performance when decoding multiple barcodes under the video streaming.

```java
void enableLatestOverlapping(@EnumCapturedResultItemType int resultItemTypes, boolean enable);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

`[in] enable`: Boolean to toggle to-the-latest overlapping on or off.

### isLatestOverlappingEnabled

Checks if to-the-latest overlapping is active for a given result item type.

```java
boolean isLatestOverlappingEnabled(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

**Return Value**

Boolean indicating the to-the-latest overlapping status for the specified type.

### setMaxOverlappingFrames

Set the maximum overlapping frames count for a given result item type. You can set it higher if:

- You capture device is stationary or moving stably.
- You want to further improve the read-rate.

```java
void setMaxOverlappingFrames(@EnumCapturedResultItemType int resultItemTypes, int maxFramesToCheck);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

`[in] maxOverlappingFrames`: The maximum overlapping frame count for the overlapping.

### getMaxOverlappingFrames

Get the maximum overlapping frames count for a given result item type.

```java
int getMaxOverlappingFrames(@EnumCapturedResultItemType int type);
```

**Parameters**

`[in] type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html?lang=android).

**Return Value**

The maximum overlapping frame count for the overlapping.

### setResultCrossVerificationCriteria

Sets the cross-verification criteria for specified result item types. This function allows customization of the multi-frame verification parameters, controlling how many frames are analyzed and how many consistent results are required.

```java
void setResultCrossVerificationCriteria(int resultItemTypes, CrossVerificationCriteria criteria);
```

**Parameters**

`[in] resultItemTypes`: Specifies the result item types with [`CapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html).

`[in] criteria`: Specifies the cross-verification criteria with a [`CrossVerificationCriteria`]({{ site.dcv_android_api }}utility/cross-verification-criteria.html) object.

**Remarks**

The default criteria per result type are:

| Result Type | `frameWindow` | `minConsistentFrames` |
| --- | --- | --- |
| Barcode (DBR) | 5 | 2 |
| Text Line (DLR) | 5 | 2 |
| Detected Quad / Deskewed Image (DDN) | 6 | 4 |

### getResultCrossVerificationCriteria

Gets the cross-verification criteria for a specified result item type.

```java
CrossVerificationCriteria getResultCrossVerificationCriteria(CapturedResultItemType resultItemType);
```

**Parameters**

`[in] resultItemType`: Specifies the result item type with [`CapturedResultItemType`]({{ site.dcv_android_api }}core/enum/captured-result-item-type.html).

**Return Value**

The cross-verification criteria for the specified result item type, of type [`CrossVerificationCriteria`]({{ site.dcv_android_api }}utility/cross-verification-criteria.html).
