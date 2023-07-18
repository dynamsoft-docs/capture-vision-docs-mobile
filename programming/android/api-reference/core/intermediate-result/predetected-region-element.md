---
layout: default-layout
Title: DSPredetectedRegionElement - Dynamsoft Core Module Android Edition API Reference
Description: The class DSPredetectedRegionElement of Dynamsoft Core Module represents a pre-detected region element, which is a subclass of DSRegionObjectElement.
Keywords: pre-detected region element, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSPredetectedRegionElement

The `DSPredetectedRegionElement` class represents a pre-detected region element, which is a subclass of `DSRegionObjectElement`.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class PredetectedRegionElement extends RegionObjectElement
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`modeName`](#modename) | *NSString \** | The name of the detection mode used to detect this region element. |

### modeName

The name of the detection mode used to detect this region element.

```java
var modeName: String { get }
```
