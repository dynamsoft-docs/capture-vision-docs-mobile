---
layout: default-layout
Title: DSVideoFrameTag - Dynamsoft Core Module iOS Edition API Reference
Description: The class DSVideoFrameTag of Dynamsoft Core Module represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the DSImageTag class and adds additional attributes and methods specific to video frames.
Keywords: video frame tag, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# DSVideoFrameTag

The `DSVideoFrameTag` class represents a video frame tag, which is a type of image tag that is used to store additional information about a video frame. It inherits from the `DSImageTag` class and adds additional attributes and methods specific to video frames.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSVideoFrameTag : DSImageTage
```
2. 
```swift
class VideoFrameTag : ImageTag
```

## Attribute Summaries

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`quality`](#quality) | *DSVideoFrameQuality* | The quality of the video frame. |
| [`isCropped`](#iscropped) | *BOOL* | Whether the video frame is cropped. |
| [`cropRegion`](#cropregion) | *CGRect* | The crop region of the video frame. |
| [`originalWidth`](#originalwidth) | *NSInteger* | The original width of the video frame. |
| [`originalHeight`](#originalheight) | *NSInteger* | The original height of the video frame. |

## Method Summaries

| Method | Description |
|------- |-------------|
| [`initWithImageId`](#initwithimageid) | The constructor of `DSVideoFrameTag`. |

## Attribute Details

### quality

The quality of the video frame.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) DSVideoFrameQuality quality;
```
2. 
```swift
var quality: EnumVideoFrameQuality { get set }
```

### isCropped

Whether the video frame is cropped.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) BOOL isCropped;
```
2. 
```swift
var isCropped: Bool { get set }
```

### cropRegion

The crop region of the video frame.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) CGRect cropRegion;
```
2. 
```swift
var cropRegion: CGRect { get set }
```

### originalWidth

The original width of the video frame.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger originalWidth;
```
2. 
```swift
var originalWidth: Int { get set }
```

### originalHeight

The original height of the video frame.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger originalHeight;
```
2. 
```swift
var originalHeight: Int { get set }
```

## Method Details

### initWithImageId

The constructor of `DSVideoFrameTag`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)initWithImageId:(NSInteger)imageId
                        quality:(DSVideoFrameQuality)quality
                      isCropped:(BOOL)isCropped
                     cropRegion:(CGRect)cropRegion
                  originalWidth:(NSInteger)originalWidth
                 originalHeight:(NSInteger)originalHeight;
```
2. 
```swift
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

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
DSVideoFrameTag *videoFrameTag = [[DSVideoFrameTag alloc] initWithImageId:imageId
                                                                 quality:quality
                                                               isCropped:isCropped
                                                              cropRegion:cropRegion
                                                           originalWidth:originalWidth
                                                          originalHeight:originalHeight];
```
2. 
```swift
let videoFrameTag = VideoFrameTag(imageId: imageId, quality: quality, isCropped: isCropped, cropRegion: cropRegion, originalWidth: originalWidth, originalHeight: originalHeight)
```
