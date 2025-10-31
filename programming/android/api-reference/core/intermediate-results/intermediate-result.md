---
layout: default-layout
title: IntermediateResult - Dynamsoft Core Module Android Edition API Reference
description: The class IntermediateResult of Dynamsoft Core Module represents a container containing a collection of IntermediateResultUnit objects.
keywords: intermediate result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResult

The `IntermediateResult` interface represents the collection of all intermediate result units produced during image processing.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class IntermediateResult
```

## Attributes

| Methods | Description |
| ------- | ----------- |
| [`getIntermediateResultUnits`](#getintermediateresultunits) | Gets an array of [`IntermediateResultUnit`](intermediate-result-unit.md) objects, each representing a different type of intermediate result. |

### getIntermediateResultUnits

Gets an array of [`IntermediateResultUnit`](intermediate-result-unit.md) objects, each representing a different type of intermediate result.

```java
IntermediateResultUnit[] getIntermediateResultUnits()
```

**Return Value**

An array of [`IntermediateResultUnit`](intermediate-result-unit.md) objects.
