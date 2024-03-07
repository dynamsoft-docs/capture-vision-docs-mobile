---
layout: default-layout
title: DSIntermediateResultReceiver - Dynamsoft Core Module iOS Edition API Reference
description: The protocol DSIntermediateResultReceiver includes methods for monitoring the output of intermediate results.
keywords: protocol, objective-c, swift
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
ignore: true
---

# DSIntermediateResultReceiver

The `DSIntermediateResultReceiver` protocol includes methods for monitoring the output of intermediate results.

## Definition

*Assembly:* DynamsoftCore.framework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@protocol DSIntermediateResultReceiver <NSObject>
```
2. 
```swift
protocol IntermediateResultReceiver: NSObjectProtocol
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getObservationParameters`](#getobservationparameters) | Get an `ObservationParameters` object to configure the observation settings. |
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

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(ObservationParameters *)getObservationParameters;
```
2. 
```swift
func getObservationParameters() -> ObservationParameters
```

**Return Value**

An `ObservationParameters` object.

### onPredetectedRegionsReceived

The method for monitoring the output of `PredetectedRegionsUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onPredetectedRegionsReceived:(PredetectedRegionsUnit *)unit
                               info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onPredetectedRegionsReceived(_ unit: PredetectedRegionsUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `PredetectedRegionsUnit` object output by the library.

`info`: The extra info of the result.

### onLocalizedBarcodesReceived

The method for monitoring the output of `LocalizedBarcodesUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onLocalizedBarcodesReceived:(LocalizedBarcodesUnit *)unit
                              info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onLocalizedBarcodesReceived(_ unit: LocalizedBarcodesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `LocalizedBarcodesUnit` object output by the library.

`info`: The extra info of the result.

### onDecodedBarcodesReceived

The method for monitoring the output of `DecodedBarcodesUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onDecodedBarcodesReceived:(DecodedBarcodesUnit *)unit
                            info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onDecodedBarcodesReceived(_ unit: DecodedBarcodesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `DecodedBarcodesUnit` object output by the library.

`info`: The extra info of the result.

### onLocalizedTextLinesReceived

The method for monitoring the output of `LocalizedTextLines`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onLocalizedTextLinesReceived:(LocalizedTextLinesUnit *)unit
                               info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onLocalizedTextLinesReceived(_ unit: LocalizedTextLinesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `LocalizedTextLines` object output by the library.

`info`: The extra info of the result.

### onRecognizedTextLinesReceived

The method for monitoring the output of `RecognizedTextLinesUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onRecognizedTextLinesReceived:(RecognizedTextLinesUnit *)unit
                                info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onRecognizedTextLinesReceived(_ unit: RecognizedTextLinesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `RecognizedTextLinesUnit` object output by the library.

`info`: The extra info of the result.

### onDetectedQuadsReceived

The method for monitoring the output of `DetectedQuadsUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onDetectedQuadsReceived:(DetectedQuadsUnit *)unit
                          info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onDetectedQuadsReceived(_ unit: DetectedQuadsUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `DetectedQuadsUnit` object output by the library.

`info`: The extra info of the result.

### onNormalizedImagesReceived

The method for monitoring the output of `NormalizedImagesUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onNormalizedImagesReceived:(NormalizedImagesUnit *)unit
                             info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onNormalizedImagesReceived(_ unit: NormalizedImagesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `NormalizedImagesUnit` object output by the library.

`info`: The extra info of the result.

### onColourImageUnitReceived

The method for monitoring the output of `ColourImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onColourImageUnitReceived:(ColourImageUnit *)unit
                            info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onColourImageUnitReceived(_ unit: ColourImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `ColourImageUnit` object output by the library.

`info`: The extra info of the result.

### onScaledDownColourImageUnitReceived

The method for monitoring the output of `ScaledDownColourImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onScaledDownColourImageUnitReceived:(ScaledDownColourImageUnit *)unit
                                      info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onScaledDownColourImageUnitReceived(_ unit: ScaledDownColourImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `ScaledDownColourImageUnit` object output by the library.

`info`: The extra info of the result.

### onGrayscaleImageUnitReceived

The method for monitoring the output of `GrayscaleImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onGrayscaleImageUnitReceived:(GrayscaleImageUnit *)unit
                               info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onGrayscaleImageUnitReceived(_ unit: GrayscaleImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `GrayscaleImageUnit` object output by the library.

`info`: The extra info of the result.

### onTransformedGrayscaleImageUnitReceived

The method for monitoring the output of `TransformedGrayscaleImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onTransformedGrayscaleImageUnitReceived:(TransformedGrayscaleImageUnit *)unit
                                          info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onTransformedGrayscaleImageUnitReceived(_ unit: TransformedGrayscaleImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `TransformedGrayscaleImageUnit` object output by the library.

`info`: The extra info of the result.

### onEnhancedGrayscaleImageUnitReceived

The method for monitoring the output of `EnhancedGrayscaleImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onEnhancedGrayscaleImageUnitReceived:(EnhancedGrayscaleImageUnit *)unit
                                       info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onEnhancedGrayscaleImageUnitReceived(_ unit: EnhancedGrayscaleImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: An `EnhancedGrayscaleImageUnit` object output by the library.

`info`: The extra info of the result.

### onBinaryImageUnitReceived

The method for monitoring the output of `BinaryImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onBinaryImageUnitReceived:(BinaryImageUnit *)unit
                            info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onBinaryImageUnitReceived(_ unit: BinaryImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `BinaryImageUnit` object output by the library.

`info`: The extra info of the result.

### onTextureDetectionResultUnitReceived

The method for monitoring the output of `TextureDetectionResultUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onTextureDetectionResultUnitReceived:(TextureDetectionResultUnit *)unit
                                       info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onTextureDetectionResultUnitReceived(_ unit: TextureDetectionResultUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `TextureDetectionResultUnit` object output by the library.

`info`: The extra info of the result.

### onTextureRemovedGrayscaleImageUnitReceived

The method for monitoring the output of `TextureRemovedGrayscaleImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onTextureRemovedGrayscaleImageUnitReceived:(TextureRemovedGrayscaleImageUnit *)unit
                                             info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onTextureRemovedGrayscaleImageUnitReceived(_ unit: TextureRemovedGrayscaleImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `TextureRemovedGrayscaleImageUnit` object output by the library.

`info`: The extra info of the result.

### onTextureRemovedBinaryImageUnitReceived

The method for monitoring the output of `TextureRemovedBinaryImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onTextureRemovedBinaryImageUnitReceived:(TextureRemovedBinaryImageUnit *)unit
                                          info:(IntermediateResultExtraInfo *)info
```
2. 
```swift
func onTextureRemovedBinaryImageUnitReceived(_ unit: TextureRemovedBinaryImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `TextureRemovedBinaryImageUnit` object output by the library.

`info`: The extra info of the result.

### onContoursUnitReceived

The method for monitoring the output of `ContoursUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onContoursUnitReceived:(ContoursUnit *)unit
                         info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onContoursUnitReceived(_ unit: ContoursUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `ContoursUnit` object output by the library.

`info`: The extra info of the result.

### onShortLinesUnitReceived

The method for monitoring the output of `ShortLinesUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onShortLinesUnitReceived:(DSShortLinesUnit*) unit
                            info:(DSIntermediateResultExtraInfo *)info;
```
2. 
```swift
func onShortLinesUnitReceived(_ unit: ShortLinesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `ShortLinesUnit` object output by the library.

`info`: The extra info of the result.

### onLineSegmentsUnitReceived

The method for monitoring the output of `LineSegmentsUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onLineSegmentsUnitReceived:(LineSegmentsUnit *)unit
                             info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onLineSegmentsUnitReceived(_ unit: LineSegmentsUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `LineSegmentsUnit` object output by the library.

`info`: The extra info of the result.

### onTextZonesUnitReceived

The method for monitoring the output of `TextZonesUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onTextZonesUnitReceived:(TextZonesUnit *)unit
                          info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onTextZonesUnitReceived(_ unit: TextZonesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `TextZonesUnit` object output by the library.

`info`: The extra info of the result.

### onTextRemovedBinaryImageUnitReceived

The method for monitoring the output of `TextRemovedBinaryImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onTextRemovedBinaryImageUnitReceived:(TextRemovedBinaryImageUnit *)unit
                                       info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onTextRemovedBinaryImageUnitReceived(_ unit: TextRemovedBinaryImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `TextRemovedBinaryImageUnit` object output by the library.

`info`: The extra info of the result.

### onLongLinesUnitReceived

The method for monitoring the output of `LongLinesUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onLongLinesUnitReceived:(LongLinesUnit *)unit
                          info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onLongLinesUnitReceived(_ unit: LongLinesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `LongLinesUnit` object output by the library.

`info`: The extra info of the result.

### onCornersUnitReceived

The method for monitoring the output of `CornersUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onCornersUnitReceived:(CornersUnit *)unit
                        info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onCornersUnitReceived(_ unit: CornersUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `CornersUnit` object output by the library.

`info`: The extra info of the result.

### onCandidateQuadEdgesUnitReceived

The method for monitoring the output of `CandidateQuadEdgesUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onCandidateQuadEdgesUnitReceived:(CandidateQuadEdgesUnit *)unit
                                   info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onCandidateQuadEdgesUnitReceived(_ unit: CandidateQuadEdgesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `CandidateQuadEdgesUnit` object output by the library.

`info`: The extra info of the result.

### onCandidateBarcodeZonesUnitReceived

The method for monitoring the output of `CandidateBarcodeZonesUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onCandidateBarcodeZonesUnitReceived:(CandidateBarcodeZonesUnit *)unit
                                      info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onCandidateBarcodeZonesUnitReceived(_ unit: CandidateBarcodeZonesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `CandidateBarcodeZonesUnit` object output by the library.

`info`: The extra info of the result.

### onScaledUpBarcodeImageUnitReceived

The method for monitoring the output of `ScaledUpBarcodeImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onScaledUpBarcodeImageUnitReceived:(ScaledUpBarcodeImageUnit *)unit
                                     info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onScaledUpBarcodeImageUnitReceived(_ unit: ScaledUpBarcodeImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `ScaledUpBarcodeImageUnit` object output by the library.

`info`: The extra info of the result.

### onDeformationResistedBarcodeImageUnitReceived

The method for monitoring the output of `DeformationResistedBarcodeImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onDeformationResistedBarcodeImageUnitReceived:(DeformationResistedBarcodeImageUnit *)unit
                                                info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onDeformationResistedBarcodeImageUnitReceived(_ unit: DeformationResistedBarcodeImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `DeformationResistedBarcodeImageUnit` object output by the library.

`info`: The extra info of the result.

### onComplementedBarcodeImageUnitReceived

The method for monitoring the output of `ComplementedBarcodeImageUnit`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onComplementedBarcodeImageUnitReceived:(ComplementedBarcodeImageUnit *)unit
                                         info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onComplementedBarcodeImageUnitReceived(_ unit: ComplementedBarcodeImageUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: A `ComplementedBarcodeImageUnit` object output by the library.

`info`: The extra info of the result.

### onTaskResultsReceived

The method for monitoring the output of `IntermediateResult`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onTaskResultsReceived:(IntermediateResult *)unit
                        info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onTaskResultsReceived(_ unit: IntermediateResult, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: An `IntermediateResult` object output by the library.

`info`: The extra info of the result.
