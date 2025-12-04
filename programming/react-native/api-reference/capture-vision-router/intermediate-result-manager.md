---
layout: default-layout
title: IntermediateResultManager Class - Dynamsoft Capture Vision React Native
description: IntermediateResultManager class of DCV React Native provides API to retrieve the intermediate results taken during the capture process.
keywords: intermediate, result, capture vision, original image, manager
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultManager

The `IntermediateResultManager` class provides the API needed to manage the intermediate results that are produced during the capture process. Currently, the `IntermediateResultManager` is mainly used for when the user wants to retrieve the original image or frame that the captured result is taken from, especially in an interactive video scenario where the input is a camera feed.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
class IntermediateResultManager
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getOriginalImage`](#getoriginalimage) | Retrieves the original image (as an ImageData object) associated with the captured result. |

### getOriginalImage

Retrieves the original image (as an ImageData object) associated with the captured result, based on the `originalImageHashId` of the [`CapturedResult`](captured-result.md).

```js
getOriginalImage(imageHashId: string): ImageData
```

**Remarks**

In order to get the hashID input parameter, please access the `originalImageHashId` of the [`CapturedResult`](captured-result.md). The `CapturedResult` can be a [`DecodedBarcodesResult`]({{ site.dbr_react_native_api }}barcode-reader/decoded-barcodes-result.html) (if the Barcode Reader is used) and so the `originalImageHashId` can be obtained from the `DecodedBarcodesResult` object directly since it extends the `CapturedResult` class.

The method returns a [`ImageData`]({{ site.dcv_react_native_api }}core/image-data.html) object which contains all the info of the original image, including a byte array to represent the raw image.

## Code Snippet

```js
let router = CaptureVisionRouter.getInstance();
let intermediateResultManager = router.getIntermediateResultManager()
router.addResultReceiver({
   onCaptureResultReceive: result => {
     let imageData = intermediateResultManager.getOriginalImage(result.originalImageHashId)
     //...
   }
});
```
