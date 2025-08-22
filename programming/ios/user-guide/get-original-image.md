---
layout: default-layout
title: Get Original Image - Dynamsoft Capture Vision iOS Edition
description: This page introduce how to get original image for Dynamsoft Capture Vision iOS Edition.
keywords: iOS, original image
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Obtain Original Image

This page is the guide of how to obtain the original image that used for data capturing.

## Use Original Image Hash ID

```swift
func onDecodedBarcodesReceived(_ result: DecodedBarcodesResult) {
    let hashId = result.originalImageHashId
    let intermediateResultManager:IntermediateResultManager = cvr.getIntermediateResultManager()
    let imageData:ImageData = intermediateResultManager.getOriginalImage(hashId)!
}
```

## Use Debug Sample

Debug sample is a simple sample for you to easily get the original image for debugging.

[View on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/ios/FoundationalAPISamples/Debug){:target="_blank"}

## Use Barcode Scanner Mobile Demo

1. Go to **Advanced Scan --> Settings**, enable the **Image Cropper**.
2. Back to scan page, click the button on the top-right corner.
3. It takes a while for capturing. When it finishes, the images are saved as a .zip file. The APP asks you how to open the file. (You can share the file via the Teams).
