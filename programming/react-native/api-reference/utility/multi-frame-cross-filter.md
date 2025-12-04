---
layout: default-layout
title: MultiFrameResultCrossFilter Class - Dynamsoft Capture Vision React Native
description: MultiFrameResultCrossFilter class of DCV React Native provides a filter for managing and filtering results.
keywords: filter, capture vision, barcode reader, react native, multiframeresultcrossfilter, result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# MultiFrameResultCrossFilter

The `MultiFrameResultCrossFilter` class is an officially implemented `CapturedResultFilter` that provides:

- **Overlapping**: Improves the read rate of multi-barcode scanning.
- **Cross Verification**: Improves the accuracy.
- **Deduplication**: Removes the duplicated results.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
class MultiFrameResultCrossFilter implements CapturedResultFilter
```

## Constructor

```js
new MultiFrameResultCrossFilter(): MultiFrameResultCrossFilter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`destroy`](#destroy) | Destroys the `MultiFrameResultCrossFilter` instance and releases the related resources on the native side. |
| [`enableLatestOverlapping`](#enablelatestoverlapping) | Enables or disables the latest overlap result filtering. |
| [`enableResultCrossVerification`](#enableresultcrossverification) | Enables or disables result cross verification for the specified result item types. |
| [`enableResultDeduplication`](#enableresultdeduplication) | Enables or disables result deduplication for the specified result item types. |
| [`getDuplicateForgetTime`](#getduplicateforgettime) | Returns the amount of time that the deduplication filter takes effect for the specified result item type(s). |
| [`getMaxOverlappingFrames`](#getmaxoverlappingframes) | Returns the maximum number of overlapping frames to check for the specified result item type(s). |
| [`isLatestOverlappingEnabled`](#islatestoverlappingenabled) | Checks if the latest overlapping filter is on for the specified result item type(s). |
| [`isResultCrossVerificationEnabled`](#isresultcrossverificationenabled) | Checks if the cross verification filter is on for the specified result item type(s). |
| [`isResultDeduplicationEnabled`](#isresultdeduplicationenabled) | Checks if the deduplication filter is on for the specified result item type(s). |
| [`setDuplicateForgetTime`](#setduplicateforgettime) | Defines the amount of time that the deduplication filter takes effect for the specified result item type(s). |
| [`setMaxOverlappingFrames`](#setmaxoverlappingframes) | Sets the maximum number of overlapping frames to check when the latest overlap filter is on. |

### destroy

Destroys the `MultiFrameResultCrossFilter` instance and releases the related resources on the native side.

```js
destroy(): void
```

### enableLatestOverlapping

Enables or disables the latest overlap result filtering. Latest overlap filtering helps in managing results that overlap in the most recent frames.

```js
enableLatestOverlapping(resultItemTypes: number, enable: boolean): any
```

**Parameters**

`resultItemTypes`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies one or multiple specific result item types.

`enable`: Whether to enable the overlapping feature.

### enableResultCrossVerification

Enables or disables result cross verification for the specified result item types (represented as a combination of [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md)). Cross verification helps in validating results across multiple frames, improving accuracy as a result.

```js
enableResultCrossVerification(resultItemTypes: number, enable: boolean): void
```

**Parameters**

`resultItemTypes`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies one or multiple specific result item types.

`enable`: Whether to enable the result cross verification.

### enableResultDeduplication

Enables or disables result deduplication for the specified result item types (represented as a combination of [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md)). If this filter is activated, the library will not scan a barcode for an amount of time again after it is scanned successfully for the first time. In order to set the amount of time that the barcode is remembered, please refer to `setDuplicateForgetTime`.

```js
enableResultDeduplication(resultItemTypes: number, enable: boolean): void
```

**Parameters**

`resultItemTypes`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies one or multiple specific result item types.

`enable`: Whether to enable the result deduplication.

### getDuplicateForgetTime

Returns the amount of time, in *milliseconds*, that the deduplication filter takes effect for the specified result item type.

```js
getMaxOverlappingFrames(type: number): Promise<number>
```

**Parameters**

`type`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies a target result item type.

### getMaxOverlappingFrames

Returns the maximum number of overlapping frames to check for the specified result item type.

```js
getMaxOverlappingFrames(type: number): Promise<number>
```

**Parameters**

`type`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies a target result item type.

### isLatestOverlappingEnabled

Checks if the latest overlapping filter is on for the specified result item type.

```js
isLatestOverlappingEnabled(type: number): Promise<boolean>
```

**Parameters**

`type`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies a target result item type.

### isResultCrossVerificationEnabled

Checks if the cross verification filter is on for the specified result item type.

```js
isResultCrossVerificationEnabled(type: number): Promise<boolean>
```

**Parameters**

`type`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies a target result item type.

### isResultDeduplicationEnabled

Checks if the deduplication filter is on for the specified result item type(s).

```js
isResultDeduplicationEnabled(type: number): Promise<boolean>
```

**Parameters**

`type`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies a target result item type.

### setDuplicateForgetTime

Defines the amount of time, in *milliseconds*, that the deduplication filter takes effect for the specified result item type(s). During this time, the library will not scan a certain barcode for the specified time after it has been scanned successfully for the first time.

```js
setDuplicateForgetTime(types: number, time: number): void
```

**Parameters**

`resultItemTypes`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies one or multiple specific result item types.

`time`: Time in milliseconds during which duplicates are disregarded.

### setMaxOverlappingFrames

Sets the maximum number of overlapping frames to check when the latest overlap filter is on for the specified result item type(s).

```js
setMaxOverlappingFrames(types: number, maxOverlappingFrames: number): void
```

**Parameters**

`resultItemTypes`: [`EnumCapturedResultItemType`](../core/enum/captured-result-item-type.md) value that specifies one or multiple specific result item types.

`maxOverlappingFrames`: The maximum overlapping frame count for the overlapping.
