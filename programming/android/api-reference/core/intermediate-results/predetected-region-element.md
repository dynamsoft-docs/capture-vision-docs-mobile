---
layout: default-layout
Title: PredetectedRegionElement - Dynamsoft Core Module Android Edition API Reference
Description: The class PredetectedRegionElement of Dynamsoft Core Module represents a pre-detected region element, which is a subclass of RegionObjectElement.
Keywords: pre-detected region element, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# PredetectedRegionElement

The `PredetectedRegionElement` class represents a pre-detected region element, which is a subclass of `RegionObjectElement`.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results
*Assembly:* DynamsoftCore.aar

```java
class PredetectedRegionElement extends RegionObjectElement
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getModeName`](#getmodename) | The name of the detection mode used to detect this region element. |

### getModeName

Get the name of the detection mode used to detect this region element.

```java
String getModeName()
```

**Return Value**

The name of the detection mode used to detect this region element.
