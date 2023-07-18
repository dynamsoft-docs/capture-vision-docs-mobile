---
layout: default-layout
Title: CapturedResultItem - Dynamsoft Core Module Android Edition API Reference
Description: The class CapturedResultItem of Dynamsoft Core Module represents an item in a captured result, such as barcode, text line, detected quad, normalized image, raw image, parsed item, etc.
Keywords: captured result item, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CapturedResultItem

The `CapturedResultItem` class represents an item in a captured result, such as barcode, text line, detected quad, normalized image, raw image, parsed item, etc.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class CapturedResultItem
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`type`](#type) | *CapturedResultItemType* | The type of the captured result item. |
| [`referencedItem`](#referenceditem) | *CapturedResultItem \** | The referenced captured result item. The reference dependencies is defined in the capture vision settings. |

### type

The type of the captured result item.

```java
var type: CapturedResultItemType { get }
```

### referencedItem

The referenced captured result item. The reference dependencies is defined in the capture vision settings.

```java
var referencedItem: CapturedResultItem? { get }
```
