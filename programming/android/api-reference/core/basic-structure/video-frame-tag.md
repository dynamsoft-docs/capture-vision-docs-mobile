---
layout: default-layout
Title: DSVideoFrameTag - Dynamsoft Core Module Android Edition API Reference
Description: The class DSVideoFrameTag of Dynamsoft Core Module represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the DSImageTag class and adds additional attributes and methods specific to video frames.
Keywords: video frame tag, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSVideoFrameTag

The `DSVideoFrameTag` class represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the `DSImageTag` class and adds additional attributes and methods specific to video frames.

## Definition

*Namespace*: com.dynamsoft.core
*Assembly:* DynamsoftCore.aar

```java
class VideoFrameTag extends ImageTag
```

## Attributes

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`quality`](#quality) | *DSVideoFrameQuality* | The quality of the video frame. |
| [`isCropped`](#iscropped) | *BOOL* | Whether the video frame is cropped. |
| [`cropRegion`](#cropregion) | *CGRect* | The crop region of the video frame. |
| [`originalWidth`](#originalwidth) | *NSInteger* | The original width of the video frame. |
| [`originalHeight`](#originalheight) | *NSInteger* | The original height of the video frame. |

## Methods

| Method | Description |
|------- |-------------|
| [`initWithImageId`](#initwithimageid) | The constructor of `DSVideoFrameTag`. |

### quality

The quality of the video frame.

```java
var quality: EnumVideoFrameQuality { get set }
```

### isCropped

Whether the video frame is cropped.

```java
var isCropped: Bool { get set }
```

### cropRegion

The crop region of the video frame.

```java
var cropRegion: CGRect { get set }
```

### originalWidth

The original width of the video frame.

```java
var originalWidth: Int { get set }
```

### originalHeight

The original height of the video frame.

```java
var originalHeight: Int { get set }
```

### initWithImageId

The constructor of `DSVideoFrameTag`.

```java
init(imageId: Int, quality: EnumVideoFrameQuality, isCropped: Bool, cropRegion: CGRect, originalWidth: Int, originalHeight: Int)
```

**Parameters**

`imageId`: The image ID of the video frame.  
`quality`: The quality of the video frame.  
`isCropped`: Whether the video frame is cropped.  
`cropRegion`: The crop region of the video frame.  
`originalWidth`: The original width of the video frame.  
`originalHeight`: The original height of the video frame.

**Return Value**

An instance of the `DSVideoFrameTag`.

**Code Snippet**

```java
let videoFrameTag = VideoFrameTag(imageId: imageId, quality: quality, isCropped: isCropped, cropRegion: cropRegion, originalWidth: originalWidth, originalHeight: originalHeight)
```
