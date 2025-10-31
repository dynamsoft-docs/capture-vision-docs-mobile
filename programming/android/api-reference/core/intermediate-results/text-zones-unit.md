---
layout: default-layout
title: TextZonesUnit - Dynamsoft Core Module Android Edition API Reference
description: The class TextZonesUnit of Dynamsoft Core Module represents a unit that contains text zones, which is derived from IntermediateResultUnit class.
keywords: text zones unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextZonesUnit

The `TextZonesUnit` class extends the `IntermediateResultUnit` class and represents a unit of text zones identified during the processing of an image. This class is used to encapsulate the locations of detected text areas within an image, providing a structured representation of where text is located.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class TextZonesUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getTextZones`](#gettextzones) | Gets an array of `TextZone` objects, each representing the geometric boundaries of a detected text zone within the image. |
| [`getCount`](#getcount) | Gets the number of text zones. |
| [`getTextZone`](#gettextzone) | Gets the text zone at the specified index. |
| [`removeAllTextZones`](#removealltextzones) | Removes all text zones. |
| [`removeTextZone`](#removetextzone) | Removes the text zone at the specified index. |
| [`addTextZone`](#addtextzone) | Adds the specified text zone. |
| [`setTextZone`](#settextzone) | Sets the text zone at the specified index. |

## Inherited Methods

The following methods are inherited from class [`IntermediateResultUnit`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`clone`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`gethashId`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image. You can use this ID to get the original image via `IntermediateResultManager` class. |
| [`getOriginalImageTag`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the image tag of the original image associated with this unit. |
| [`getType`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`EnumIntermediateResultUnitType`]({{ site.dcv_android_api }}core/enum/intermediate-result-unit-type.html?lang=android). |
| [`getTransformMatrix`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`EnumTransformMatrixType`]({{ site.dcv_android_api }}core/enum/transform-matrix-type.html). |
| [`replace`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the old unit with the new unit. |

### getTextZones

Gets an array of `TextZone` objects, each representing the geometric boundaries of a detected text zone within the image.

```java
@Nullable
TextZone[] getTextZones()
```

**Return Value**

The array of `TextZone` objects.

### getCount

Gets the number of text zones.

```java
int getCount()
```

**Return Value**

The number of text zones.

### getTextZone

Gets the text zone at the specified index.

```java
@Nullable
TextZone getTextZone(int index)
```

**Parameters**

`[in] index`: The index of the text zone.

**Return Value**

A `TextZone` object as the text zone at the specified index.

### removeAllTextZones

Removes all text zones.

```java
void removeAllTextZones()
```

### removeTextZone

Removes the text zone at the specified index.

```java
int removeTextZone(int index)
```

**Parameters**

`[in] index`: The index of the text zone.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addTextZone

Adds the specified text zone.

```java
int addTextZone(TextZone textZone, Matrix matrixToOriginalImage)
```

**Parameters**

`[in] textZone`: The text zone to be added.

`[in] matrixToOriginalImage`: The transformation matrix to the original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setTextZone

Sets the text zone at the specified index.

```java
int setTextZone(int index, TextZone textZone, Matrix matrixToOriginalImage)
```

**Parameters**

`[in] index`: The index of the text zone.

`[in] textZone`: The text zone to be set.

`[in] matrixToOriginalImage`: The transformation matrix to the original image.

**Return Value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
