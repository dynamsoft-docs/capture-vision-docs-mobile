---
layout: default-layout
Title: CaptureStateListener - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The protocol CaptureStateListener of Dynamsoft Capture Vision Router Module defines the methods for monitoring the capture state.
Keywords: capture state, monitoring, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CaptureStateListener

The `CaptureStateListener` protocol defines the methods for monitoring the capture state.

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

`state`: One of the `CaptureState` value that indicates the capture state.
