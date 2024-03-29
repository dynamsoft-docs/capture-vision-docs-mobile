---
layout: default-layout
title: CaptureStateListener - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The interface CaptureStateListener of Dynamsoft Capture Vision Router Module defines the methods for monitoring the capture state.
keywords: capture state, monitoring, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CaptureStateListener

The `CaptureStateListener` interface defines the methods for monitoring the capture state.

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionRouter.aar

```java
interface CaptureStateListener
```

## Methods

| Method | Description |
|------- |-------------|
| [`onCapturedStateChanged`](#oncapturedstatechanged) | The method for monitoring the capture state. |

### onCapturedStateChanged

The method for monitoring the capture state.

```java
void onCaptureStateChanged(EnumCaptureState state);
```

**Parameters**

`[in] state`: One of the [`EnumCaptureState`]({{site.dcv_enumerations}}capture-vision-router/capture-state.html) value that indicates the capture state.
