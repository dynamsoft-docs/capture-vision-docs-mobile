---
layout: default-layout
Title: DSContoursUnit - Dynamsoft Core Module Android Edition API Reference
Description: The class DSContoursUnit of Dynamsoft Core Module represents a unit that contains contours as intermediate results.
Keywords: contours unit, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSContoursUnit

The `DSContoursUnit` class represents a unit that contains contours as intermediate results. It is derived from the `DSIntermediateResultUnit` class.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class ContoursUnit: IntermediateResultUnit
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`contours`](#contours) | *NSArray <DSContour**>* | A array of `DSContour` objects. |

### contours

A array of `DSContour` objects.

```java
var contours: [Contour]? { get set }
```
