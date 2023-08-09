---
layout: default-layout
Title: ImageSourceStateListener - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The interface ImageSourceStateListener of Dynamsoft Capture Vision Router Module defines methods for monitoring the state of the ImageSourceAdapter.
Keywords: image source state listener, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ImageSourceStateListener

The `ImageSourceStateListener` interface defines methods for monitoring the state of the ImageSourceAdapter.

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionRouter.aar

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
void onImageSourceStateReceived(EnumImageSourceState status);
```

**Parameters**

`[in] state`: One of the [`EnumImageSourceState`]({{site.enums}}core/image-source-state.html)` that indicates the state of the ImageSourceAdapter.