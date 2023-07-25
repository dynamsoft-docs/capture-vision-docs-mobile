---
layout: default-layout
Title: IntermediateResultReceiver - Dynamsoft Core Module Android Edition API Reference
Description: The protocol IntermediateResultReceiver includes methods for monitoring the output of intermediate results.
Keywords: protocol, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# IntermediateResultReceiver

The `IntermediateResultReceiver` protocol includes methods for monitoring the output of intermediate results.

## Definition

*Namespace:* com.dynamsoft.core.intermediate_results
*Assembly:* DynamsoftCore.aar

```java
interface IntermediateResultReceiver
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getObservationParameters`](#getobservationparameters) | Get a `ObservationParameters` object to configure the observation settings. |
| [`onPredetectedRegionsReceived`](#onpredetectedregionsreceived) | The method for monitoring the output of `PredetectedRegionsUnit`. |
| [`onLocalizedBarcodesReceived`](#onlocalizedbarcodesreceived) | The method for monitoring the output of `LocalizedBarcodesUnit`. |
| [`onDecodedBarcodesReceived`](#ondecodedbarcodesreceived) | The method for monitoring the output of `DecodedBarcodesUnit`. |
| [`onLocalizedTextLinesReceived`](#onlocalizedtextlinesreceived) | The method for monitoring the output of `LocalizedTextLinesUnit`. |
| [`onRecognizedTextLinesReceived`](#onrecognizedtextlinesreceived) | The method for monitoring the output of `RecognizedTextLinesUnit`. |
| [`onDetectedQuadsReceived`](#ondetectedquadsreceived) | The method for monitoring the output of `DetectedQuadsUnit`. |
| [`onNormalizedImagesReceived`](#onnormalizedimagesreceived) | The method for monitoring the output of `NormalizedImagesUnit`. |
| [`onColourImageUnitReceived`](#oncolourimageunitreceived) | The method for monitoring the output of `ColourImageUnit`. |
| [`onScaledDownColourImageUnitReceived`](#onscaleddowncolourimageunitreceived) | The method for monitoring the output of `ScaledDownColourImageUnit`. |
| [`onGrayscaleImageUnitReceived`](#ongrayscaleimageunitreceived) | The method for monitoring the output of `GrayscaleImageUnit`. |
| [`onTransformedGrayscaleImageUnitReceived`](#ontransformedgrayscaleimageunitreceived) | The method for monitoring the output of `TransformedGrayscaleImageUnit`. |
| [`onEnhancedGrayscaleImageUnitReceived`](#onenhancedgrayscaleimageunitreceived) | The method for monitoring the output of `EnhancedGrayscaleImageUnit`. |
| [`onBinaryImageUnitReceived`](#onbinaryimageunitreceived) | The method for monitoring the output of `BinaryImageUnit`. |
| [`onTextureDetectionResultUnitReceived`](#ontexturedetectionresultunitreceived) | The method for monitoring the output of `TextureDetectionResultUnit`. |
| [`onTextureRemovedGrayscaleImageUnitReceived`](#ontextureremovedgrayscaleimageunitreceived) | The method for monitoring the output of `TextureRemovedGrayscaleImageUnit`. |
| [`onTextureRemovedBinaryImageUnitReceived`](#ontextureremovedbinaryimageunitreceived) | The method for monitoring the output of `TextureRemovedBinaryImageUnit`. |
| [`onContoursUnitReceived`](#oncontoursunitreceived) | The method for monitoring the output of `ContoursUnit`. |
| [`onLineSegmentsUnitReceived`](#onlinesegmentsunitreceived) | The method for monitoring the output of `LineSegmentsUnit`. |
| [`onTextZonesUnitReceived`](#ontextzonesunitreceived) | The method for monitoring the output of `TextZonesUnit`. |
| [`onTextRemovedBinaryImageUnitReceived`](#ontextremovedbinaryimageunitreceived) | The method for monitoring the output of `TextRemovedBinaryImageUnit`. |
| [`onLongLinesUnitReceived`](#onlonglinesunitreceived) | The method for monitoring the output of `LongLinesUnit`. |
| [`onCornersUnitReceived`](#oncornersunitreceived) | The method for monitoring the output of `CornersUnit`. |
| [`onCandidateQuadEdgesUnitReceived`](#oncandidatequadedgesunitreceived) | The method for monitoring the output of `CandidateQuadEdgesUnit`. |
| [`onCandidateBarcodeZonesUnitReceived`](#oncandidatebarcodezonesunitreceived) | The method for monitoring the output of `CandidateBarcodeZonesUnit`. |
| [`onScaledUpBarcodeImageUnitReceived`](#onscaledupbarcodeimageunitreceived) | The method for monitoring the output of `ScaledUpBarcodeImageUnit`. |
| [`onDeformationResistedBarcodeImageUnitReceived`](#ondeformationresistedbarcodeimageunitreceived) | The method for monitoring the output of `DeformationResistedBarcodeImageUnit`. |
| [`onComplementedBarcodeImageUnitReceived`](#oncomplementedbarcodeimageunitreceived) | The method for monitoring the output of `ComplementedBarcodeImageUnit`. |
| [`onTaskResultsReceived`](#ontaskresultsreceived) | The method for monitoring the output of task results. |

### getObservationParameters

Get a `ObservationParameters` object to configure the observation settings.

```java
ObservationParameters getObservationParameters();
```

**Return Value**

An `ObservationParameters` object.

### onPredetectedRegionsReceived

The method for monitoring the output of `PredetectedRegionsUnit`.

```java
void onPredetectedRegionsReceived(PredetectedRegionsUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `PredetectedRegionsUnit` object output by the library.
`info`: The extra info of the result.

### onLocalizedBarcodesReceived

The method for monitoring the output of `LocalizedBarcodesUnit`.

```java
void onLocalizedBarcodesReceived(LocalizedBarcodesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `LocalizedBarcodesUnit` object output by the library.
`info`: The extra info of the result.

### onDecodedBarcodesReceived

The method for monitoring the output of `DecodedBarcodesUnit`.

```java
void onDecodedBarcodesReceived(DecodedBarcodesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `DecodedBarcodesUnit` object output by the library.
`info`: The extra info of the result.

### onLocalizedTextLinesReceived

The method for monitoring the output of `LocalizedTextLines`.

```java
void onLocalizedTextLinesReceived(LocalizedTextLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `LocalizedTextLines` object output by the library.
`info`: The extra info of the result.

### onRecognizedTextLinesReceived

The method for monitoring the output of `RecognizedTextLinesUnit`.

```java
void onRecognizedTextLinesReceived(RecognizedTextLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `RecognizedTextLinesUnit` object output by the library.
`info`: The extra info of the result.

### onDetectedQuadsReceived

The method for monitoring the output of `DetectedQuadsUnit`.

```java
void onDetectedQuadsReceived(DetectedQuadsUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `DetectedQuadsUnit` object output by the library.
`info`: The extra info of the result.

### onNormalizedImagesReceived

The method for monitoring the output of `NormalizedImagesUnit`.

```java
void onNormalizedImagesReceived(NormalizedImagesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `NormalizedImagesUnit` object output by the library.
`info`: The extra info of the result.

### onColourImageUnitReceived

The method for monitoring the output of `ColourImageUnit`.

```java
void onColourImageUnitReceived(ColourImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `ColourImageUnit` object output by the library.
`info`: The extra info of the result.

### onScaledDownColourImageUnitReceived

The method for monitoring the output of `ScaledDownColourImageUnit`.

```java
void onScaledDownColourImageUnitReceived(ScaledDownColourImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `ScaledDownColourImageUnit` object output by the library.
`info`: The extra info of the result.

### onGrayscaleImageUnitReceived

The method for monitoring the output of `GrayscaleImageUnit`.

```java
void onGrayscaleImageUnitReceived(GrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `GrayscaleImageUnit` object output by the library.
`info`: The extra info of the result.

### onTransformedGrayscaleImageUnitReceived

The method for monitoring the output of `TransformedGrayscaleImageUnit`.

```java
void onTransformedGrayscaleImageUnitReceived(TransformedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `TransformedGrayscaleImageUnit` object output by the library.
`info`: The extra info of the result.

### onEnhancedGrayscaleImageUnitReceived

The method for monitoring the output of `EnhancedGrayscaleImageUnit`.

```java
void onEnhancedGrayscaleImageUnitReceived(EnhancedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: An `EnhancedGrayscaleImageUnit` object output by the library.
`info`: The extra info of the result.

### onBinaryImageUnitReceived

The method for monitoring the output of `BinaryImageUnit`.

```java
void onBinaryImageUnitReceived(BinaryImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `BinaryImageUnit` object output by the library.
`info`: The extra info of the result.

### onTextureDetectionResultUnitReceived

The method for monitoring the output of `TextureDetectionResultUnit`.

```java
void onTextureDetectionResultUnitReceived(TextureDetectionResultUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `TextureDetectionResultUnit` object output by the library.
`info`: The extra info of the result.

### onTextureRemovedGrayscaleImageUnitReceived

The method for monitoring the output of `TextureRemovedGrayscaleImageUnit`.

```java
void onTextureRemovedGrayscaleImageUnitReceived(TextureRemovedGrayscaleImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `TextureRemovedGrayscaleImageUnit` object output by the library.
`info`: The extra info of the result.

### onTextureRemovedBinaryImageUnitReceived

The method for monitoring the output of `TextureRemovedBinaryImageUnit`.

```java
void onTextureRemovedBinaryImageUnitReceived(TextureRemovedBinaryImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `TextureRemovedBinaryImageUnit` object output by the library.
`info`: The extra info of the result.

### onContoursUnitReceived

The method for monitoring the output of `ContoursUnit`.

```java
void onContoursUnitReceived(ContoursUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `ContoursUnit` object output by the library.
`info`: The extra info of the result.

### onLineSegmentsUnitReceived

The method for monitoring the output of `LineSegmentsUnit`.

```java
void onLineSegmentsUnitReceived(LineSegmentsUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `LineSegmentsUnit` object output by the library.
`info`: The extra info of the result.

### onTextZonesUnitReceived

The method for monitoring the output of `TextZonesUnit`.

```java
void onTextZonesUnitReceived(TextZonesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `TextZonesUnit` object output by the library.
`info`: The extra info of the result.

### onTextRemovedBinaryImageUnitReceived

The method for monitoring the output of `TextRemovedBinaryImageUnit`.

```java
void onTextRemovedBinaryImageUnitReceived(TextRemovedBinaryImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `TextRemovedBinaryImageUnit` object output by the library.
`info`: The extra info of the result.

### onLongLinesUnitReceived

The method for monitoring the output of `LongLinesUnit`.

```java
void onLongLinesUnitReceived(LongLinesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `LongLinesUnit` object output by the library.
`info`: The extra info of the result.

### onCornersUnitReceived

The method for monitoring the output of `CornersUnit`.

```java
void onCornersUnitReceived(CornersUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `CornersUnit` object output by the library.
`info`: The extra info of the result.

### onCandidateQuadEdgesUnitReceived

The method for monitoring the output of `CandidateQuadEdgesUnit`.

```java
void onCandidateQuadEdgesUnitReceived(CandidateQuadEdgesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `CandidateQuadEdgesUnit` object output by the library.
`info`: The extra info of the result.

### onCandidateBarcodeZonesUnitReceived

The method for monitoring the output of `CandidateBarcodeZonesUnit`.

```java
void onCandidateBarcodeZonesUnitReceived(CandidateBarcodeZonesUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `CandidateBarcodeZonesUnit` object output by the library.
`info`: The extra info of the result.

### onScaledUpBarcodeImageUnitReceived

The method for monitoring the output of `ScaledUpBarcodeImageUnit`.

```java
void onScaledUpBarcodeImageUnitReceived(ScaledUpBarcodeImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `ScaledUpBarcodeImageUnit` object output by the library.
`info`: The extra info of the result.

### onDeformationResistedBarcodeImageUnitReceived

The method for monitoring the output of `DeformationResistedBarcodeImageUnit`.

```java
void onDeformationResistedBarcodeImageUnitReceived(DeformationResistedBarcodeImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `DeformationResistedBarcodeImageUnit` object output by the library.
`info`: The extra info of the result.

### onComplementedBarcodeImageUnitReceived

The method for monitoring the output of `ComplementedBarcodeImageUnit`.

```java
void onComplementedBarcodeImageUnitReceived(ComplementedBarcodeImageUnit unit, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: A `ComplementedBarcodeImageUnit` object output by the library.
`info`: The extra info of the result.

### onTaskResultsReceived

The method for monitoring the output of `IntermediateResult`.

```java
void onTaskResultsReceived(IntermediateResult result, IntermediateResultExtraInfo info);
```

**Parameters**

`unit`: An `IntermediateResult` object output by the library.
`info`: The extra info of the result.
