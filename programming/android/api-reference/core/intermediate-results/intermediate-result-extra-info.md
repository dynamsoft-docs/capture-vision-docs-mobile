---
layout: default-layout
Title: IntermediateResultExtraInfo - Dynamsoft Core Module Android Edition API Reference
Description: The class IntermediateResultExtraInfo of Dynamsoft Core Module represents the extra information for generating an intermediate result unit, which contains the name of the TargetROIDef object, the name of the task object, whether the intermediate result is section-level result, and the type of the section that generates the intermediate result.
Keywords: intermediate result extra info, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultExtraInfo

The `IntermediateResultExtraInfo` class represents the extra information for generating an intermediate result unit, which contains the name of the TargetROIDef object, the name of the task object, whether the intermediate result is section-level result, and the type of the section that generates the intermediate result.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results
*Assembly:* DynamsoftCore.aar

```java
class IntermediateResultExtraInfo
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`targetROIDefName`](#targetroidefname) | *String* | The name of the TargetROIDef object that generates the intermediate result. |
| [`taskName`](#taskname) | *String* | The name of the task object that generates the intermediate result. |
| [`isSectionLevelResult`](#issectionlevelresult) | *boolean* | Whether the intermediate result is section-level result. |
| [`sectionType`](#sectiontype) | *[EnumSectionType]({{ site.enums }}core/section-type.html?lang=android)* | The type of the section that generates the intermediate result. |

### targetROIDefName

The name of the TargetROIDef object that generates the intermediate result.

```java
String targetROIDefName;
```

### taskName

The name of the task object that generates the intermediate result.

```java
String taskName;
```

### isSectionLevelResult

Whether the intermediate result is section-level result.

```java
boolean isSectionLevelResult;
```

### sectionType

The type of the section that generates the intermediate result.

```java
EnumSectionType sectionType;
```
