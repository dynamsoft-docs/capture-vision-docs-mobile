---
layout: default-layout
title: Add Resource Files - Dynamsoft Capture Vision Android Edition
description: This page introduce how to get original image for Dynamsoft Capture Vision Android Edition.
keywords: Android, original image
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
---

# Obtain Original Image

This page is the guide of how to obtain the original image that used for data capturing.

## Use Original Image Hash ID

```java
mRouter.addResultReceiver(new CapturedResultReceiver() {
    @Override
    public void onDecodedBarcodesReceived(@NonNull DecodedBarcodesResult result) {
        String hashID = result.getOriginalImageHashId();
        IntermediateResultManager intermediateResultManager = mRouter.getIntermediateResultManager();
        ImageData data = intermediateResultManager.getOriginalImage(hashID);
    }
});
```

## Use Debug Sample

Debug sample is a simple sample for you to easily get the original image for debugging.

[View on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/FoundationalAPISamples/Debug){:target="_blank"}

## Use Barcode Scanner Mobile Demo

1. Go to **Advanced Scan --> Settings**, enable the **Image Cropper**.
2. Back to scan page, click the button on the top-right corner.
3. It takes a while for capturing. When it finishes, the images are saved as a .zip file. The APP asks you how to open the file. (You can share the file via the Teams).
