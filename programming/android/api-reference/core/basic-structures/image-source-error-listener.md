---
layout: default-layout
title: ImageSourceErrorListener - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The interface ImageSourceErrorListener of Dynamsoft Capture Vision Router Module defines methods for monitoring the errors that occur in the ImageSourceAdapter.
keywords: Error listener, ImageSourceAdapter, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceErrorListener

The `ImageSourceErrorListener` interface that defines methods for monitoring the errors that occur in the [`ImageSourceAdapter`](image-source-adapter.md).

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
interface ImageSourceErrorListener 
```

## Methods

| Method | Description |
|------- |-------------|
| [`onErrorReceived`](#onerrorreceived) | The callback method for monitoring the errors that occur in the [`ImageSourceAdapter`](image-source-adapter.md). |

### onErrorReceived

The callback method for monitoring the errors that occur in the [`ImageSourceAdapter`](image-source-adapter.md).

```java
void onErrorReceived(int errorCode, String errorMessage);
```
