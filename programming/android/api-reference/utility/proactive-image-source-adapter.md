---
layout: default-layout
title: ProactiveImageSourceAdapter - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: The class ProactiveImageSourceAdapter of Dynamsoft Capture Vision Router Module is an abstract class that provides an interface for proactively fetching images in a separate thread.
keywords: Proactive image source adapter, Android
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# ProactiveImageSourceAdapter

The `ProactiveImageSourceAdapter` class is an abstract base class that extends the `ImageSourceAdapter` class. It provides an interface for proactively fetching images in a separate thread.

## Definition

*Namespace:* com.dynamsoft.utility

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
abstract class ProactiveImageSourceAdapter extends ImageSourceAdapter
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`setImageFetchInterval`](#setimagefetchinterval) | Sets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer. |
| [`getImageFetchInterval`](#getimagefetchinterval) | Gets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer. |

### setImageFetchInterval

Sets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer.

```java
void setImageFetchInterval(int milliseconds);
```

**Parameters**

`[in] milliseconds`: The time interval in milliseconds.

### getImageFetchInterval

Gets the time interval for the ImageSource to wait before attempting to fetch another image to put in the buffer.

```java
int getImageFetchInterval();
```

**Return Value**

The time interval in milliseconds.
