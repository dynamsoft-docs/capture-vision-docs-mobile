---
layout: default-layout
title: VideoFrameTag - Dynamsoft Core Module Android Edition API Reference
description: The class VideoFrameTag of Dynamsoft Core Module represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the ImageTag class and adds additional attributes and methods specific to video frames.
keywords: video frame tag, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# VideoFrameTag

The `VideoFrameTag` class represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the `ImageTag` class and adds additional attributes and methods specific to video frames.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCore.aar

```java
class VideoFrameTag extends ImageTag
```

## Methods

| Methods | Description |
| ---------- | ----------- |
| [`getQuality`](#getquality) | Get the quality of the video frame. |
| [`isCropped`](#iscropped) | Check whether the video frame is cropped. |
| [`getCropRegion`](#getcropregion) | Get the crop region of the video frame. |
| [`getOriginalWidth`](#getoriginalwidth) | Get the original width of the video frame. |
| [`getOriginalHeight`](#getoriginalheight) | Get the original height of the video frame. |
| [`VideoFrameTag(frameID,quality,isCropped,cropRegion,originalWidth,originalHeight)`](#videoframetagframeidqualityiscroppedcropregionoriginalwidthoriginalheight) | The constructor. |

### getQuality

The quality of the video frame.

```java
EnumFrameQuality getQuality();
```

### isCropped

Whether the video frame is cropped.

```java
boolean isCropped();
```

### getCropRegion

The crop region of the video frame.

```java
Rect getCropRegion();
```

### getOriginalWidth

The original width of the video frame.

```java
int getOriginalWidth();
```

### getOriginalHeight

The original height of the video frame.

```java
int getOriginalHeight();
```

### VideoFrameTag(frameID,quality,isCropped,cropRegion,originalWidth,originalHeight)

The constructor.

```java
VideoFrameTag(int frameID, EnumFrameQuality quality, boolean isCropped, Rect cropRegion, int originalWidth, int originalHeight);
```

**Parameters**

`[in] frameID`: The image ID of the video frame.  

`[in] quality`: The quality of the video frame.  

`[in] isCropped`: Whether the video frame is cropped.  

`[in] cropRegion`: The crop region of the video frame.  

`[in] originalWidth`: The original width of the video frame.  

`[in] originalHeight`: The original height of the video frame.
