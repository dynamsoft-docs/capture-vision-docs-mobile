---
layout: default-layout
title: BufferedItemsManager - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The BufferedItemsManager class of DCV Android edition is used to manage the buffered items.
keywords: buffered items, manager, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# BufferedItemsManager

The `BufferedItemsManager` class is used to manage the buffered items.

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class BufferedItemsManager
```

## Methods

| Method | Description |
|------- |-------------|
| [`setMaxBufferedItems`](#setmaxbuffereditems) | Set the maximum number of buffered items. |
| [`getMaxBufferedItems`](#getmaxbuffereditems) | Get the maximum number of buffered items. |
| [`getBufferedCharacterItemSet`](#getbufferedcharacteritemset) | Get the buffered item set. |

### setMaxBufferedItems

Set the maximum number of buffered items.

```java
void setMaxBufferedItems(int count);
```

**Parameters**

`[in] count`: The maximum number of buffered items.

### getMaxBufferedItems

Get the maximum number of buffered items.

```java
int getMaxBufferedItems();
```

**Return Value**

The maximum number of buffered items.

### getBufferedCharacterItemSet

Get the buffered item set.

```java
BufferedCharacterItemSet getBufferedCharacterItemSet();
```

**Return Value**

The buffered item set.
