---
layout: default-layout
title: VideoFrameTag - Dynamsoft Capture Vision Android Edition API Reference
description: The class VideoFrameTag of Dynamsoft Capture Vision Android represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the ImageTag class and adds additional attributes and methods specific to video frames.
keywords: video frame tag, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# VideoFrameTag

The `VideoFrameTag` class represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the `ImageTag` class and adds additional attributes and methods specific to video frames.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class VideoFrameTag extends ImageTag
```

## Methods

| Methods | Description |
| ---------- | ----------- |
| [`getClarity`](#getquality) | Gets the clarity of the video frame. |
| [`getQuality`](#getquality) | Gets the quality of the video frame. |
| [`isCropped`](#iscropped) | Checks whether the video frame is cropped. |
| [`getCropRegion`](#getcropregion) | Gets the crop region of the video frame. |
| [`getOriginalWidth`](#getoriginalwidth) | Gets the original width of the video frame. |
| [`setOriginalWidth`](#setoriginalwidth) | Sets the original width of the video frame. |
| [`getOriginalHeight`](#getoriginalheight) | Gets the original height of the video frame. |
| [`setOriginalHeight`](#setoriginalheight) | Sets the original height of the video frame. |
| [`VideoFrameTag`](#videoframetag) | The constructor. |
| [`VideoFrameTag(imageID,distanceMode,quality,isCropped,cropRegion,originalWidth,originalHeight)`](#videoframetagframeidqualityiscroppedcropregionoriginalwidthoriginalheight) | Constructs a VideoFrameTag from the specified parameters. |

### getClarity

Gets the clarity of the video frame.

```java
int getClarity();
```

### getQuality

Gets the quality of the video frame.

```java
@EnumVideoFrameQuality
int getQuality();
```

### isCropped

Whether the video frame is cropped.

```java
boolean isCropped();
```

### getCropRegion

Gets the crop region of the video frame.

```java
Rect getCropRegion();
```

### getOriginalWidth

Gets the original width of the video frame.

```java
int getOriginalWidth();
```

### setOriginalWidth

Sets the original width of the video frame.

```java
void setOriginalWidth(int originalWidth);
```

### getOriginalHeight

Gets the original height of the video frame.

```java
int getOriginalHeight();
```

### setOriginalHeight

Sets the original height of the video frame.

```java
void setOriginalHeight(int originalHeight);
```

### VideoFrameTag(imageID,distanceMode,quality,isCropped,cropRegion,originalWidth,originalHeight)

The constructor.

```java
VideoFrameTag(int imageId, @EnumImageCaptureDistanceMode int distanceMode, @EnumVideoFrameQuality int quality, boolean isCropped, Rect cropRegion, int originalWidth, int originalHeight);
```

**Parameters**

`[in] frameID`: The image ID of the video frame.  

`[in] quality`: The quality of the video frame.  

`[in] isCropped`: Whether the video frame is cropped.  

`[in] cropRegion`: The crop region of the video frame.  

`[in] originalWidth`: The original width of the video frame.  

`[in] originalHeight`: The original height of the video frame.
