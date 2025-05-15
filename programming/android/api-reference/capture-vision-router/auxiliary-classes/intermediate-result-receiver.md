---
layout: default-layout
title: IntermediateResultReceiver - Dynamsoft Core Module Android Edition API Reference
description: The interface IntermediateResultReceiver includes methods for monitoring the output of intermediate results.
keywords: interface, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultReceiver

The `IntermediateResultReceiver` class is designed as a standardized way for retrieving intermediate results in image processing workflows in the Dynamsoft Capture Vision architecture. By implementing the `CapturedResultReceiver`, you will receive the callback of the various types of captured results, such as pre-detected regions, localized barcodes, etc. Each callback is optional, allowing flexibility and customization based on the needs of the application.

## Definition

*Namespace:* com.dynamsoft.cvr

*Assembly:* DynamsoftCaptureVisionRouter.aar

```java
interface IntermediateResultReceiver
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getObservationParameters`](#getobservationparameters) | Gets the observed parameters of the intermediate result receiver. |
| [`onTargetROIResultsReceived`](#ontargetroiresultsreceived) | The callback triggered when the processing of a target-ROI is finished. |
| [`onTaskResultsReceived`](#ontaskresultsreceived) | The callback triggered when the processing of a task is finished. |
| [`onPredetectedRegionsReceived`](#onpredetectedregionsreceived) | The callback triggered when pre-detected regions are received. |
| [`onLocalizedBarcodesReceived`](#onlocalizedbarcodesreceived) | The callback triggered when localized barcodes are received. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The callback triggered when decoded barcodes are received. |
| [`onLocalizedTextLinesReceived`](#onlocalizedtextlinesreceived) | The callback triggered when localized text lines are received. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The callback triggered when recognized text lines are received. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | The callback triggered when detected quads are received. |
| [`onDeskewedImagesReceived`](#ondeskewedimagesreceived) | The callback triggered when deskewed images are received. |
| [`onEnhancedImageReceived`](#onenhancedimagesreceived) | The callback triggered when enhanced images are received. |
| [`onColourImageUnitReceived`](#oncolourimageunitreceived) | The callback triggered when a colour image unit is received. |
| [`onScaledColourImageUnitReceived`](#onscaledcolourimageunitreceived) | The callback triggered when a scaled-down colour image unit is received. |
| [`onGrayscaleImageUnitReceived`](#ongrayscaleimageunitreceived) | The callback triggered when a grayscale image unit is received. |
| [`onTransformedGrayscaleImageUnitReceived`](#ontransformedgrayscaleimageunitreceived) | The callback triggered when a transformed grayscale image unit is received. |
| [`onEnhancedGrayscaleImageUnitReceived`](#onenhancedgrayscaleimageunitreceived) | The callback triggered when an enhanced grayscale image unit is received. |
| [`onBinaryImageUnitReceived`](#onbinaryimageunitreceived) | The callback triggered when a binary image unit is received. |
| [`onTextureDetectionResultUnitReceived`](#ontexturedetectionresultunitreceived) | The callback triggered when a texture detection result unit is received. |
| [`onTextureRemovedGrayscaleImageUnitReceived`](#ontextureremovedgrayscaleimageunitreceived) | The callback triggered when a texture-removed grayscale image unit is received. |
| [`onTextureRemovedBinaryImageUnitReceived`](#ontextureremovedbinaryimageunitreceived) | The callback triggered when a texture-removed binary image unit is received. |
| [`onContoursUnitReceived`](#oncontoursunitreceived) | The callback triggered when a contours unit is received. |
| [`onLineSegmentsUnitReceived`](#onlinesegmentsunitreceived) | The callback triggered when a line segments unit is received. |
| [`onTextZonesUnitReceived`](#ontextzonesunitreceived) | The callback triggered when a text zones unit is received. |
| [`onTextRemovedBinaryImageUnitReceived`](#ontextremovedbinaryimageunitreceived) | The callback triggered when a text-removed binary image unit is received. |
| [`onShortLinesUnitReceived`](#onshortlinesunitreceived) | The callback triggered when a short lines unit is received. |
| [`onLogicLinesUnitReceived`](#onlogiclinesunitreceived) | The callback triggered when a logic lines unit is received. |
| [`onLongLinesUnitReceived`](#onlonglinesunitreceived) | The callback triggered when a long lines unit is received. |
| [`onCornersUnitReceived`](#oncornersunitreceived) | The callback triggered when a corners unit is received. |
| [`onCandidateQuadEdgesUnitReceived`](#oncandidatequadedgesunitreceived) | The callback triggered when a candidate quad edges unit are detected. |
| [`onCandidateBarcodeZonesUnitReceived`](#oncandidatebarcodezonesunitreceived) | The callback triggered when a candidate barcode zones unit are detected. |
| [`onScaledBarcodeImageUnitReceived`](#onscaledbarcodeimageunitreceived) | The callback triggered when a scaled-up barcode image unit is received. |
| [`onDeformationResistedBarcodeImageUnitReceived`](#ondeformationresistedbarcodeimageunitreceived) | The callback triggered when a deformation-resisted barcode image unit is received. |
| [`onComplementedBarcodeImageUnitReceived`](#oncomplementedbarcodeimageunitreceived) | The callback triggered when a complemented barcode image unit is received. |
| [`onRawTextLinesUnitReceived`](#onrawtextlinesunitreceived) | The callback triggered when a raw text lines unit is received. |

### getObservationParameters

Gets the observed parameters of the intermediate result receiver.

```java
ObservationParameters getObservationParameters();
```

**Return Value**

An `ObservationParameters` object.

### onTargetROIResultsReceived

The callback triggered when the processing of a target-ROI is finished.

```java
void onTargetROIResultsReceived(@NonNull IntermediateResult result, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result from the task, of type `IntermediateResult`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTaskResultsReceived

The callback triggered when the processing of a task is finished.

```java
void onTaskResultsReceived(@NonNull IntermediateResult result, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result from the task, of type `IntermediateResult`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onPredetectedRegionsReceived

The callback triggered when pre-detected regions are received.

```java
void onPredetectedRegionsReceived(@NonNull PredetectedRegionsUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the pre-detected regions, of type `PredetectedRegionsUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLocalizedBarcodesReceived

The callback triggered when localized barcodes are received.

```java
void onLocalizedBarcodesReceived(@NonNull LocalizedBarcodesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the localized barcodes, of type `LocalizedBarcodesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDecodedBarcodesReceived

The callback triggered when decoded barcodes are received.

```java
void onDecodedBarcodesReceived(@NonNull DecodedBarcodesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the decoded barcodes, of type `DecodedBarcodesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLocalizedTextLinesReceived

The callback triggered when localized text lines are received.

```java
void onLocalizedTextLinesReceived(@NonNull LocalizedTextLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the localized text lines, of type `LocalizedTextLinesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onRecognizedTextLinesReceived

The callback triggered when recognized text lines are received.

```java
void onRecognizedTextLinesReceived(@NonNull RecognizedTextLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the recognized text lines, of type `RecognizedTextLinesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDetectedQuadsReceived

The callback triggered when detected quads are received.

```java
void onDetectedQuadsReceived(@NonNull DetectedQuadsUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the detected quads, of type `DetectedQuadsUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDeskewedImagesReceived

The callback triggered when deskewed images are received.

```java
void onDeskewedImagesReceived(@NonNull DeskewedImagesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the deskewed images, of type `DeskewedImagesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onEnhancedImagesReceived

The callback triggered when enhanced images are received.

```java
void onEnhancedImagesReceived(@NonNull EnhancedImagesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the enhanced images, of type `EnhancedImagesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onColourImageUnitReceived

The callback triggered when colour images are received.

```java
void onColourImageUnitReceived(@NonNull ColourImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the colour image, of type `ColourImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onScaledColourImageUnitReceived

The callback triggered when scaled-down colour images are received.

```java
void onScaledColourImageUnitReceived(@NonNull ScaledColourImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the scaled-down colour image, of type `ScaledColourImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onGrayscaleImageUnitReceived

The callback triggered when grayscale images are received.

```java
void onGrayscaleImageUnitReceived(@NonNull GrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the grayscale image, of type `GrayscaleImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTransformedGrayscaleImageUnitReceived

The callback triggered when transformed grayscale images are received.

```java
void onTransformedGrayscaleImageUnitReceived(@NonNull TransformedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the transformed grayscale image, of type `TransformedGrayscaleImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onEnhancedGrayscaleImageUnitReceived

The callback triggered when enhanced grayscale images are received.

```java
void onEnhancedGrayscaleImageUnitReceived(@NonNull EnhancedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the enhanced grayscale image, of type `EnhancedGrayscaleImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onBinaryImageUnitReceived

The callback triggered when binary images are received.

```java
void onBinaryImageUnitReceived(@NonNull BinaryImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the binary image, of type `BinaryImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextureDetectionResultUnitReceived

The callback triggered when texture detection results are received.

```java
void onTextureDetectionResultUnitReceived(@NonNull TextureDetectionResultUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the texture detection result, of type `TextureDetectionResultUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextureRemovedGrayscaleImageUnitReceived

The callback triggered when texture removed grayscale images are received.

```java
void onTextureRemovedGrayscaleImageUnitReceived(@NonNull TextureRemovedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the texture removed grayscale image, of type `TextureRemovedGrayscaleImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextureRemovedBinaryImageUnitReceived

The callback triggered when texture removed binary images are received.

```java
void onTextureRemovedBinaryImageUnitReceived(@NonNull TextureRemovedBinaryImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the texture removed binary image, of type `TextureRemovedBinaryImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onContoursUnitReceived

The callback triggered when contours are received.

```java
void onContoursUnitReceived(@NonNull ContoursUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the contours, of type `ContoursUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLineSegmentsUnitReceived

The callback triggered when line segments are received.

```java
void onLineSegmentsUnitReceived(@NonNull LineSegmentsUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the line segments, of type `LineSegmentsUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextZonesUnitReceived

The callback triggered when text zones are received.

```java
void onTextZonesUnitReceived(@NonNull TextZonesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the text zones, of type `TextZonesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextRemovedBinaryImageUnitReceived

The callback triggered when text removed binary images are received.

```java
void onTextRemovedBinaryImageUnitReceived(@NonNull TextRemovedBinaryImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the text removed binary image, of type `TextRemovedBinaryImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onShortLinesUnitReceived

The callback triggered when short lines are received.

```java
void onShortLinesUnitReceived(@NonNull ShortLinesUnit unit IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the short lines, of type `ShortLinesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLogicLinesUnitReceived

The callback triggered when logic lines are received.

```java
void onLogicLinesUnitReceived(@NonNull LongLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the long lines, of type `LongLinesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLongLinesUnitReceived

The callback triggered when long lines are received.

```java
void onLongLinesUnitReceived(@NonNull LongLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the long lines, of type `LongLinesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onCornersUnitReceived

The callback triggered when corners are received.

```java
void onCornersUnitReceived(@NonNull CornersUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the corners, of type `CornersUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onCandidateQuadEdgesUnitReceived

The callback triggered when candidate quad edges are received.

```java
void onCandidateQuadEdgesUnitReceived(@NonNull CandidateQuadEdgesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the candidate quad edges, of type `CandidateQuadEdgesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onCandidateBarcodeZonesUnitReceived

The callback triggered when candidate barcode zones are received.

```java
void onCandidateBarcodeZonesUnitReceived(@NonNull CandidateBarcodeZonesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the candidate barcode zones, of type `CandidateBarcodeZonesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onScaledBarcodeImageUnitReceived

The callback triggered when scaled up barcode images are received.

```java
void onScaledBarcodeImageUnitReceived(@NonNull ScaledBarcodeImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the scaled up barcode image, of type `ScaledBarcodeImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDeformationResistedBarcodeImageUnitReceived

The callback triggered when deformation resisted barcode images are received.

```java
void onDeformationResistedBarcodeImageUnitReceived(@NonNull DeformationResistedBarcodeImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the deformation resisted barcode image, of type `DeformationResistedBarcodeImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onComplementedBarcodeImageUnitReceived

The callback triggered when complemented barcode images are received.

```java
void onComplementedBarcodeImageUnitReceived(@NonNull ComplementedBarcodeImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the complemented barcode image, of type `ComplementedBarcodeImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onRawTextLinesUnitReceived

The callback triggered when a raw text lines unit is received.

```java
void onRawTextLinesUnitReceived(@NonNull RawTextLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The intermediate result that contains the raw text lines, of type `RawTextLinesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.
