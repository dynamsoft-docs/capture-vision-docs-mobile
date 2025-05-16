---
layout: default-layout
title: IntermediateResultExtraInfo - Dynamsoft Core Module Android Edition API Reference
description: The class IntermediateResultExtraInfo of Dynamsoft Core Module represents the extra information for generating an intermediate result unit, which contains the name of the TargetROIDef object, the name of the task object, whether the intermediate result is section-level result, and the type of the section that generates the intermediate result.
keywords: intermediate result extra info, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultExtraInfo

The `IntermediateResultExtraInfo` class represents the extra information associated with an intermediate result. It includes properties such as the target ROI definition name, task name, section level result indicator, and section type.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class IntermediateResultExtraInfo
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`targetROIDefName`](#targetroidefname) | *String* | The property indicates the name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) object that generates the intermediate result. |
| [`taskName`](#taskname) | *String* | The property indicates the name of the processing task to which this result belongs. |
| [`isSectionLevelResult`](#issectionlevelresult) | *boolean* | The property indicates whether the result is at the section level. |
| [`sectionType`](#sectiontype) | *[EnumSectionType]({{ site.dcv_android_api }}core/enum/section-type.html?lang=android)* | The property indicates the type of section that generates the result, if applicable, as defined by the enumeration `EnumSectionType`. |

### targetROIDefName

The name of the [`TargetROIDef`]({{ site.dcv_parameters_reference }}target-roi-def/) object that generates the intermediate result.

```java
String targetROIDefName;
```

### taskName

The name of the processing task to which this result belongs.

```java
String taskName;
```

### isSectionLevelResult

The property indicates whether the result is at the section level.

```java
boolean isSectionLevelResult;
```

### sectionType

The type of section that generates the result, if applicable, as defined by the enumeration [`EnumSectionType`]({{ site.dcv_android_api }}core/enum/section-type.html?lang=android).

```java
EnumSectionType sectionType;
```
