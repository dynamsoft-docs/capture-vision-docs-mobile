---
layout: default-layout
title: ImageSourceStateListener - Dynamsoft Capture Vision Android Edition API Reference
description: The interface ImageSourceStateListener of Dynamsoft Capture Vision Android defines methods for monitoring the state of the ImageSourceAdapter.
keywords: image source state listener, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceStateListener

The `ImageSourceStateListener` interface defines methods for monitoring the state of the ImageSourceAdapter.

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
interface ImageSourceStateListener
```

## Methods

| Method | Description |
|------- |-------------|
| [`onImageSourceStateReceived`](#onimagesourcestatereceived) | The methods for monitoring the state of the ImageSourceAdapter. |

### onImageSourceStateReceived

The methods for monitoring the state of the ImageSourceAdapter.

```java
void onImageSourceStateReceived(@EnumImageSourceState int status);
```

**Parameters**

`[in] state`: One of the [`EnumImageSourceState`]({{ site.dcv_android_api }}core/enum/image-source-state.html)` that indicates the state of the ImageSourceAdapter.
