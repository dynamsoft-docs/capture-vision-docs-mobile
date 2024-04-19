---
layout: default-layout
title: PredetectedRegionsUnit - Dynamsoft Core Module Android Edition API Reference
description: The class PredetectedRegionsUnit of Dynamsoft Core Module represents a unit that contains a collection of pre-detected regions.
keywords: pre-detected regions, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# PredetectedRegionsUnit

The `PredetectedRegionsUnit` class extends the `IntermediateResultUnit` class and represents a unit of intermediate result specifically for pre-detected regions.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class PredetectedRegionsUnit extends IntermediateResultUnit
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getPredetectedRegions`](#getpredetectedregions) | Gets an array of `PredetectedRegionElement` objects, each representing a pre-detected region detected within the image. |
| [`getCount`](#getcount) | Get the number of `PredetectedRegionElement` objects. |
| [`getPredetectedRegion`](#getpredetectedregion) | Get the `PredetectedRegionElement` object at the specified index. |
| [`removeAllPredetectedRegions`](#removeallpredetectedregions) | Remove all `PredetectedRegionElement` objects. |
| [`removePredetectedRegion`](#removepredetectedregion) | Remove the `PredetectedRegionElement` object at the specified index. |
| [`addPredetectedRegion`](#addpredetectedregion) | Add a `PredetectedRegionElement` object. |
| [`setPredetectedRegion`](#setpredetectedregion) | Set the `PredetectedRegionElement` object at the specified index. |

## Inherited Methods

The following methods are inherited from class [`IntermediateResultUnit`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html).

| Method | Description |
|------- |-------------|
| [`clone`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#clone) | Creates a copy of the intermediate result unit. |
| [`gethashId`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gethashid) | Gets the hash ID of the unit. The hash ID is the unique identifier for the intermediate result unit. |
| [`getOriginalImageHashId`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagehashid) | Gets the hash ID of the original image. You can use this ID to get the original image via `IntermediateResultManager` class. |
| [`getOriginalImageTag`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#getoriginalimagetag) | Gets the image tag of the original image associated with this unit. |
| [`getType`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gettype) | Gets the type of the intermediate result unit, defined by the enumeration [`EnumIntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=android). |
| [`getTransformMatrix`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#gettransformmatrix) | Gets the transformation matrix via [`EnumTransformMatrixType`]({{site.dcv_enumerations}}/core/transform-matrix-type.html). |
| [`replace`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html#replace) | Replaces the old unit with the new unit. |

### getPredetectedRegions

Get the array of `PredetectedRegionElement` objects.

```java
PredetectedRegionElement[] getPredetectedRegions();
```

**Return Value**

The array of [`PredetectedRegionElement`](predetected-region-element.md) objects.

### getCount

Get the number of `PredetectedRegionElement` objects.

```java
int getCount();
```

**Return Value**

The number of `PredetectedRegionElement` objects.

### getPredetectedRegion

Get the `PredetectedRegionElement` object at the specified index.

```java
PredetectedRegionElement getPredetectedRegion(int index);
```

**Return Value**

The `PredetectedRegionElement` object at the specified index.

### removeAllPredetectedRegions

Remove all `PredetectedRegionElement` objects.

```java
void removeAllPredetectedRegions();
```

### removePredetectedRegion

Remove the `PredetectedRegionElement` object at the specified index.

```java
int removePredetectedRegion(int index);
```

**Return Value**

The index of the removed `PredetectedRegionElement` object.

### addPredetectedRegion

Add a `PredetectedRegionElement` object.

```java
int addPredetectedRegion(PredetectedRegionElement element, Matrix matrixToOriginalImage);
```

**Return Value**

The index of the added `PredetectedRegionElement` object.

### setPredetectedRegion

Set the `PredetectedRegionElement` object at the specified index.

```java
int setPredetectedRegion(int index, PredetectedRegionElement element, Matrix matrixToOriginalImage);
```

**Return Value**

The index of the set `PredetectedRegionElement` object.
