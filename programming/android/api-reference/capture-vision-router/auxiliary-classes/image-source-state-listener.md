---
layout: default-layout
Title: DSImageSourceStateListener - Dynamsoft Capture Vision Router Module Android Edition API Reference
Description: The protocol DSImageSourceStateListener of Dynamsoft Capture Vision Router Module defines methods for monitoring the state of the ImageSourceAdapter.
Keywords: image source state listener, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSImageSourceStateListener

The `DSImageSourceStateListener` protocol defines methods for monitoring the state of the ImageSourceAdapter.

## Definition

*Namespace*: com.dynamsoft.cvr
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

`state`: One of the DSImageSourceState that indicates the state of the ImageSourceAdapter.
