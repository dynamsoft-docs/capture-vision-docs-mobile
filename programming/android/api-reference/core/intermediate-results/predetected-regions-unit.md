---
layout: default-layout
Title: PredetectedRegionsUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class PredetectedRegionsUnit of Dynamsoft Core Module represents a unit that contains a collection of pre-detected regions.
Keywords: pre-detected regions, Java, Kotlin
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
class PredetectedRegionsUnit: IntermediateResultUnit
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getPredetectedRegions`](#getpredetectedregions) | Get the array of `PredetectedRegionElement` objects. |

### getPredetectedRegions

Get the array of `PredetectedRegionElement` objects.

```java
PredetectedRegionElement[] getPredetectedRegions();
```

**Return Value**

The array of [`PredetectedRegionElement`](predetected-region-element.md) objects.
