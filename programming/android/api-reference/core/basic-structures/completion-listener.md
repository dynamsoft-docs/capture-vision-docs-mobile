---
layout: default-layout
title: CompletionListener - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The interface CompletionListener of Dynamsoft Capture Vision Router Module defines the methods for handling callback when startCapturing is finished.
keywords: startCapturing, completion, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CompletionListener

The `CompletionListener` interface defines methods to receive callback when [`startCapturing`](../../capture-vision-router/multiple-file-processing.html#startcapturing) method is finished.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
interface CompletionListener
```

## Methods

| Method | Description |
|------- |-------------|
| [`onSuccess`](#onsuccess) | The methods is triggered when the `startCapturing` succeed. |
| [`onFailure`](#onfailure) | The methods is triggered when the `startCapturing` failed. |

### onSuccess

The methods is triggered when the `startCapturing` is success.

```java
void onSuccess();
```

### onFailure

The methods is triggered when the `startCapturing` failed.

```java
void onFailure(int errorCode, String errorMessage);
```

**Parameters**

`[in] errorCode`: The error code that describes why the `startCapturing` failed.

`[in] errorMessage`: The error message that describes why the `startCapturing` failed.
