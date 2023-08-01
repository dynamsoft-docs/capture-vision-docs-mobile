---
layout: default-layout
Title: TextZonesUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class TextZonesUnit of Dynamsoft Core Module represents a unit that contains text zones, which is derived from IntermediateResultUnit class.
Keywords: text zones unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextZonesUnit

The `TextZonesUnit` class represents a unit that contains text zones, which is derived from `IntermediateResultUnit` class.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCore.aar

```java
class TextZonesUnit extends IntermediateResultUnit
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getTextZones`](#gettextzones) | Gets the array of `Quadrilaterals` as text zones. |

### getTextZones

Gets the array of `Quadrilaterals` as text zones.

```java
Quadrilateral[] getTextZones()
```

**Return Value**

The array of `Quadrilaterals` as text zones.