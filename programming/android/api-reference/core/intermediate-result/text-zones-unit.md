---
layout: default-layout
Title: DSTextZonesUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class DSTextZonesUnit of Dynamsoft Core Module represents a unit that contains text zones, which is derived from DSIntermediateResultUnit class.
Keywords: text zones unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSTextZonesUnit

The `DSTextZonesUnit` class represents a unit that contains text zones, which is derived from `DSIntermediateResultUnit` class.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class TextZonesUnit: IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`textZones`](#textzones) | *NSArray<DSQuadrilateral *> \** | An array of DSQuadrilaterals as text zones. |

### textZones

An array of DSQuadrilaterals as text zones.

```java
var textZones: [Quadrilateral]? { get set }
```
