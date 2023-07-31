---
layout: default-layout
Title: CapturedResultItem - Dynamsoft Core Module Android Edition API Reference
Description: The class CapturedResultItem of Dynamsoft Core Module represents an item in a captured result, such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.
Keywords: captured result item, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultItem

The `CapturedResultItem` class represents an item in a captured result, such as barcode, text line, detected quad, normalized image, original image, parsed item, etc.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures
*Assembly:* DynamsoftCore.aar

```java
class CapturedResultItem
```

## Attributes

| Method | Description |
| ------ | ----------- |
| [`getType`](#gettype) | Get the type of the captured result item. |
| [`getReferencedItem`](#getreferenceditem) | Get the referenced captured result item. The reference dependencies is defined in the capture vision settings. |

### getType

Get the type of the captured result item.

```java
EnumCapturedResultItemType getType();
```

**Return Value**

The type of the captured result item.

### getReferencedItem

Get the referenced captured result item. The reference dependencies is defined in the capture vision settings.

```java
CapturedResultItem getReferencedItem();
```

**Return Value**

The referenced captured result item.
