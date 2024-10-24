---
layout: default-layout
title: MultiFrameResultCrossFilter Class - Dynamsoft Capture Vision MAUI Edition
description: MultiFrameResultCrossFilter class of DCV MAUI edition implements the CapturedResultFilter interface, providing filtering options for various types of captured results.
keywords: filter, CapturedResultFilter, deduplication, cross verification, duplicate forget time
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# MultiFrameResultCrossFilter

The `MultiFrameResultCrossFilter` class implements the `CapturedResultFilter` interface, providing filtering options for various types of captured results.

## Definition

*Namespace:* Dynamsoft.Utility.Maui

*Assembly:* Dynamsoft.CaptureVisionRouter.Maui

```csharp
class MultiFrameResultCrossFilter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`MultiFrameResultCrossFilter`](#multiframeresultcrossfilter-1) | The constructor. |
| [`EnableResultDeduplication`](#enableresultdeduplication) | Enables or disables the deduplication process for one or multiple specific result item types. |
| [`EnableResultCrossVerification`](#enableresultcrossverification) | Enables or disables the verification of one or multiple specific result item types. |
| [`SetDuplicateForgetTime`](#setduplicateforgettime) | Sets the interval during which duplicates are disregarded for specific result item types. |
| [`IsResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Checks if deduplication is active for a given result item type. |
| [`IsResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Checks if verification is active for a given result item type. |
| [`GetDuplicateForgetTime`](#getduplicateforgettime) | Gets the interval during which duplicates are disregarded for specific result item types. |

### MultiFrameResultCrossFilter

The constructor.

```csharp
MultiFrameResultCrossFilter();
```

### EnableResultCrossVerification

Enables or disables the verification of one or multiple specific result item types.

```csharp
void EnableResultCrossVerification(EnumCapturedResultItemType resultItemTypes, bool enable);
```

**Parameters**

`resultItemTypes`: Specifies one or multiple specific result item types, which can be defined using [`EnumCapturedResultItemType`]({{ site.dcv_maui_api }}core/enum/captured-result-item-type.html).

`enable`: A BOOL value that indicates whether to enable the result cross verification feature.

### IsResultCrossVerificationEnabled

Checks if verification is active for a given result item type.

```csharp
bool IsResultCrossVerificationEnabled(EnumCapturedResultItemType type);
```

**Parameters**

`type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_maui_api }}core/enum/captured-result-item-type.html).

**Return Value**

Boolean indicating the status of verification for the specified type.

### EnableResultDeduplication

Enables or disables the deduplication process for one or multiple specific result item types.

```csharp
void EnableResultDeduplication(EnumCapturedResultItemType resultItemTypes, bool enable);
```

**Parameters**

`resultItemTypes`: Specifies one or multiple specific result item types, which can be defined using [`EnumCapturedResultItemType`]({{ site.dcv_maui_api }}core/enum/captured-result-item-type.html).

`enable`: A BOOL value that indicates whether to enable the result deduplication feature.

### IsResultDeduplicationEnabled

Checks if deduplication is active for a given result item type.

```csharp
bool IsResultDeduplicationEnabled(EnumCapturedResultItemType type);
```

**Parameters**

`type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_maui_api }}core/enum/captured-result-item-type.html).

**Return Value**

Boolean indicating the deduplication status for the specified type.

### SetDuplicateForgetTime

Sets the interval during which duplicates are disregarded for specific result item types.

```csharp
void SetDuplicateForgetTime(EnumCapturedResultItemType resultItemTypes, int time);
```

**Parameters**

`resultItemTypes`: Specifies one or multiple specific result item types, which can be defined using [`EnumCapturedResultItemType`]({{ site.dcv_maui_api }}core/enum/captured-result-item-type.html).

`time`: The duplicate forget time of the specified capture result type.

### GetDuplicateForgetTime

Gets the interval during which duplicates are disregarded for specific result item types.

```csharp
int GetDuplicateForgetTime(EnumCapturedResultItemType type);
```

**Parameters**

`type`: Specifies the result item type with [`EnumCapturedResultItemType`]({{ site.dcv_maui_api }}core/enum/captured-result-item-type.html).

**Return Value**

The set interval for the specified item type.
