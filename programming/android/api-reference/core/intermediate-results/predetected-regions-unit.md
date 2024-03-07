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

The `PredetectedRegionsUnit` class represents a unit that contains a collection of pre-detected regions.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class PredetectedRegionsUnit extends IntermediateResultUnit
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getPredetectedRegions`](#getpredetectedregions) | Get the array of `PredetectedRegionElement` objects. |
| [`getCount`](#getcount) | Get the number of `PredetectedRegionElement` objects. |
| [`getPredetectedRegion`](#getpredetectedregion) | Get the `PredetectedRegionElement` object at the specified index. |
| [`removeAllPredetectedRegions`](#removeallpredetectedregions) | Remove all `PredetectedRegionElement` objects. |
| [`removePredetectedRegion`](#removepredetectedregion) | Remove the `PredetectedRegionElement` object at the specified index. |
| [`addPredetectedRegion`](#addpredetectedregion) | Add a `PredetectedRegionElement` object. |
| [`setPredetectedRegion`](#setpredetectedregion) | Set the `PredetectedRegionElement` object at the specified index. |

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
