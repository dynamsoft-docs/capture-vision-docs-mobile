---
layout: default-layout
Title: DSIntermediateResultExtraInfo - Dynamsoft Core Module Android Edition API Reference
Description: The class DSIntermediateResultExtraInfo of Dynamsoft Core Module represents the extra information for generating an intermediate result unit, which contains the name of the TargetROIDef object, the name of the task object, whether the intermediate result is section-level result, and the type of the section that generates the intermediate result.
Keywords: intermediate result extra info, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSIntermediateResultExtraInfo

The `DSIntermediateResultExtraInfo` class represents the extra information for generating an intermediate result unit, which contains the name of the TargetROIDef object, the name of the task object, whether the intermediate result is section-level result, and the type of the section that generates the intermediate result.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class IntermediateResultExtraInfo
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`targetROIDefName`](#targetroidefname) | *NSString \** | The name of the TargetROIDef object that generates the intermediate result. |
| [`taskName`](#taskname) | *NSString \** | The name of the task object that generates the intermediate result. |
| [`isSectionLevelResult`](#issectionlevelresult) | *bool \** | Whether the intermediate result is section-level result. |
| [`sectionType`](#sectiontype) | *EnumSectionType* | The type of the section that generates the intermediate result. |

### targetROIDefName

The name of the TargetROIDef object that generates the intermediate result.

```java
var targetROIDefName: String { get }
```

### taskName

The name of the task object that generates the intermediate result.

```java
var taskName: String { get }
```

### isSectionLevelResult

Whether the intermediate result is section-level result.

```java
var isSectionLevelResult: Bool { get }
```

### sectionType

The type of the section that generates the intermediate result.

```java
var sectionType: EnumSectionType { get }
```
