---
layout: default-layout
title: IntermediateResultReceiver - Dynamsoft Core Module Android Edition API Reference
description: The interface IntermediateResultReceiver includes methods for monitoring the output of intermediate results.
keywords: interface, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# IntermediateResultReceiver

> You are reading a history page of `DynamsoftCore`. Start from v3.2.10, the `IntermediateResultReceiver` class is moved to the `DynamsoftCaptureVisionRouter` module. View the [`DynamsoftCaptureVisionRouter.IntermediateResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html) for the latest version.

The `IntermediateResultReceiver` interface includes methods for monitoring the output of intermediate results.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
interface IntermediateResultReceiver
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getObservationParameters`](#getobservationparameters) | Gets the observed parameters of the intermediate result receiver. Allowing for configuration of intermediate result observation. |
| [`onPredetectedRegionsReceived`](#onpredetectedregionsreceived) | The callback method triggered when a pre-detected regions unit is received. |
| [`onLocalizedBarcodesReceived`](#onlocalizedbarcodesreceived) | The callback method triggered when a localized barcodes unit is received. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The callback method triggered when a decoded barcodes unit is received. |
| [`onLocalizedTextLinesReceived`](#onlocalizedtextlinesreceived) | The callback method triggered when a localized text lines unit is received. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The callback method triggered when a recognized text lines unit is received. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | The callback method triggered when a detected quads unit is received. |
| [`onNormalizedImagesReceived`](#onnormalizedimagesreceived) | The callback method triggered when a normalized images unit is received. |
| [`onColourImageUnitReceived`](#oncolourimageunitreceived) | The callback method triggered when a colour images unit is received. |
| [`onScaledDownColourImageUnitReceived`](#onscaleddowncolourimageunitreceived) | The callback method triggered when a scaled down colour images unit is received. |
| [`onGrayscaleImageUnitReceived`](#ongrayscaleimageunitreceived) | The callback method triggered when a grayscale images unit is received. |
| [`onTransformedGrayscaleImageUnitReceived`](#ontransformedgrayscaleimageunitreceived) | The callback method triggered when a transformed grayscale images unit is received. |
| [`onEnhancedGrayscaleImageUnitReceived`](#onenhancedgrayscaleimageunitreceived) | The callback method triggered when a enhanced grayscale images unit is received. |
| [`onBinaryImageUnitReceived`](#onbinaryimageunitreceived) | The callback method triggered when a binary images unit is received. |
| [`onTextureDetectionResultUnitReceived`](#ontexturedetectionresultunitreceived) | The callback method triggered when a texture detection results unit is received. |
| [`onTextureRemovedGrayscaleImageUnitReceived`](#ontextureremovedgrayscaleimageunitreceived) | The callback method triggered when a texture-removed grayscale images unit is received. |
| [`onTextureRemovedBinaryImageUnitReceived`](#ontextureremovedbinaryimageunitreceived) | The callback method triggered when a texture-removed binary images unit is received. |
| [`onContoursUnitReceived`](#oncontoursunitreceived) | The callback method triggered when a contours unit is received. |
| [`onLineSegmentsUnitReceived`](#onlinesegmentsunitreceived) | The callback method triggered when a line segments unit is received. |
| [`onTextZonesUnitReceived`](#ontextzonesunitreceived) | The callback method triggered when a text zones unit is received. |
| [`onTextRemovedBinaryImageUnitReceived`](#ontextremovedbinaryimageunitreceived) | The callback method triggered when a text removed binary images unit is received. |
| [`onLongLinesUnitReceived`](#onlonglinesunitreceived) | The callback method triggered when a long lines unit is received. |
| [`onCornersUnitReceived`](#oncornersunitreceived) | The callback method triggered when a corners unit is received. |
| [`onCandidateQuadEdgesUnitReceived`](#oncandidatequadedgesunitreceived) | The callback method triggered when a candidate quad edges unit is received. |
| [`onCandidateBarcodeZonesUnitReceived`](#oncandidatebarcodezonesunitreceived) | The callback method triggered when a candidate barcode zones unit is received. |
| [`onScaledUpBarcodeImageUnitReceived`](#onscaledupbarcodeimageunitreceived) | The callback method triggered when a scaled up barcode images unit is received. |
| [`onDeformationResistedBarcodeImageUnitReceived`](#ondeformationresistedbarcodeimageunitreceived) | The callback method triggered when a deformation-resisted barcode images unit is received. |
| [`onComplementedBarcodeImageUnitReceived`](#oncomplementedbarcodeimageunitreceived) | The callback method triggered when a complemented barcode images unit is received. |
| [`onTaskResultsReceived`](#ontaskresultsreceived) | The callback method triggered when a task results unit is received. |

### getObservationParameters

Gets the observed parameters of the intermediate result receiver. Allowing for configuration of intermediate result observation.

```java
ObservationParameters getObservationParameters();
```

**Return Value**

The observed parameters, of type `ObservationParameters`. The default parameters are to observe all intermediate result unit types and all tasks.

### onPredetectedRegionsReceived

The callback method triggered when a pre-detected regions unit is received.

```java
void onPredetectedRegionsReceived(PredetectedRegionsUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the pre-detected regions, of type `PredetectedRegionsUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLocalizedBarcodesReceived

The callback method triggered when a localized barcodes unit is received.

```java
void onLocalizedBarcodesReceived(LocalizedBarcodesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the localized barcodes, of type `LocalizedBarcodesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDecodedBarcodesReceived

The callback method triggered when a decoded barcodes unit is received.

```java
void onDecodedBarcodesReceived(DecodedBarcodesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the decoded barcodes, of type `DecodedBarcodesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLocalizedTextLinesReceived

The callback method triggered when a localized text lines unit is received.

```java
void onLocalizedTextLinesReceived(LocalizedTextLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the localized text lines, of type `LocalizedTextLinesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onRecognizedTextLinesReceived

The callback method triggered when a recognized text lines unit is received.

```java
void onRecognizedTextLinesReceived(RecognizedTextLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the recognized text lines, of type `RecognizedTextLinesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDetectedQuadsReceived

The callback method triggered when a detected quads unit is received.

```java
void onDetectedQuadsReceived(DetectedQuadsUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the detected quads, of type `DetectedQuadsUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onNormalizedImagesReceived

The callback method triggered when a normalized images unit is received.

```java
void onNormalizedImagesReceived(NormalizedImagesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the normalized images, of type `NormalizedImagesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onColourImageUnitReceived

The callback method triggered when a colour images unit is received.

```java
void onColourImageUnitReceived(ColourImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the colour images, of type `ColourImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onScaledDownColourImageUnitReceived

The callback method triggered when a scaled-down colour images unit is received.

```java
void onScaledDownColourImageUnitReceived(ScaledDownColourImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the scaled-down colour images, of type `ScaledDownColourImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onGrayscaleImageUnitReceived

The callback method triggered when a grayscale images unit is received.

```java
void onGrayscaleImageUnitReceived(GrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the grayscale images, of type `GrayscaleImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTransformedGrayscaleImageUnitReceived

The callback method triggered when a transformed grayscale images unit is received.

```java
void onTransformedGrayscaleImageUnitReceived(TransformedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the transformed grayscale images, of type `TransformedGrayscaleImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onEnhancedGrayscaleImageUnitReceived

The callback method triggered when a enhanced grayscale images unit is received.

```java
void onEnhancedGrayscaleImageUnitReceived(EnhancedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the enhanced grayscale images, of type `EnhancedGrayscaleImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onBinaryImageUnitReceived

The callback method triggered when a binary images unit is received.

```java
void onBinaryImageUnitReceived(BinaryImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the binary images, of type `BinaryImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextureDetectionResultUnitReceived

The callback method triggered when a texture detection results unit is received.

```java
void onTextureDetectionResultUnitReceived(TextureDetectionResultUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the texture detection results, of type `TextureDetectionResultUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextureRemovedGrayscaleImageUnitReceived

The callback method triggered when a texture removed grayscale images unit is received.

```java
void onTextureRemovedGrayscaleImageUnitReceived(TextureRemovedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the texture removed grayscale images, of type `TextureRemovedGrayscaleImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextureRemovedBinaryImageUnitReceived

The callback method triggered when a texture removed binary images unit is received.

```java
void onTextureRemovedBinaryImageUnitReceived(TextureRemovedBinaryImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the texture removed binary images, of type `TextureRemovedBinaryImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onContoursUnitReceived

The callback method triggered when a contours unit is received.

```java
void onContoursUnitReceived(ContoursUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the contours, of type `ContoursUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLineSegmentsUnitReceived

The callback method triggered when a line segments unit is received.

```java
void onLineSegmentsUnitReceived(LineSegmentsUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the line segments, of type `LineSegmentsUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextZonesUnitReceived

The callback method triggered when a text zones unit is received.

```java
void onTextZonesUnitReceived(TextZonesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the text zones, of type `TextZonesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextRemovedBinaryImageUnitReceived

The callback method triggered when a text removed binary images unit is received.

```java
void onTextRemovedBinaryImageUnitReceived(TextRemovedBinaryImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the text removed binary images, of type `TextRemovedBinaryImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLongLinesUnitReceived

The callback method triggered when a long lines unit is received.

```java
void onLongLinesUnitReceived(LongLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the long lines, of type `LongLinesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onCornersUnitReceived

The callback method triggered when a corners unit is received.

```java
void onCornersUnitReceived(CornersUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the corners, of type `CornersUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onCandidateQuadEdgesUnitReceived

The callback method triggered when a candidate quad edges unit is received.

```java
void onCandidateQuadEdgesUnitReceived(CandidateQuadEdgesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the candidate quad edges, of type `CandidateQuadEdgesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onCandidateBarcodeZonesUnitReceived

The callback method triggered when a candidate barcode zones unit is received.

```java
void onCandidateBarcodeZonesUnitReceived(CandidateBarcodeZonesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the candidate barcode zones, of type `CandidateBarcodeZonesUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onScaledUpBarcodeImageUnitReceived

The callback method triggered when a scaled up barcode images unit is received.

```java
void onScaledUpBarcodeImageUnitReceived(ScaledUpBarcodeImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the scaled up barcode images, of type `ScaledUpBarcodeImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDeformationResistedBarcodeImageUnitReceived

The callback method triggered when a deformation resisted barcode images unit is received.

```java
void onDeformationResistedBarcodeImageUnitReceived(DeformationResistedBarcodeImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the deformation resisted barcode images, of type `DeformationResistedBarcodeImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onComplementedBarcodeImageUnitReceived

The callback method triggered when a complemented barcode images unit is received.

```java
void onComplementedBarcodeImageUnitReceived(ComplementedBarcodeImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the complemented barcode images, of type `ComplementedBarcodeImageUnit`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTaskResultsReceived

The callback method triggered when a task results unit is received.

```java
void onTaskResultsReceived(IntermediateResult result, IntermediateResultExtraInfo info);
```

**Parameters**

`[in] unit`: The result unit that contains the task results, of type `IntermediateResult`.

`[in] info`: Additional information about the result, of type `IntermediateResultExtraInfo`.
