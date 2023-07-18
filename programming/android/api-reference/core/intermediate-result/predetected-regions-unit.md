---
layout: default-layout
Title: DSPredetectedRegionsUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class DSPredetectedRegionsUnit of Dynamsoft Core Module represents a unit that contains a collection of pre-detected regions.
Keywords: pre-detected regions, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSPredetectedRegionsUnit

The `DSPredetectedRegionsUnit` class represents a unit that contains a collection of pre-detected regions.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class PredetectedRegionsUnit: IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`predetectedRegions`](#predetectedregions) | *NSArray<DSPredetectedRegionElement*> \** | An array of `DSPredetectedRegionElement` objects. |

### predetectedRegions

An array of `DSPredetectedRegionElement` objects.

```java
var predetectedRegions: [PredetectedRegionElement]? { get set }
```
