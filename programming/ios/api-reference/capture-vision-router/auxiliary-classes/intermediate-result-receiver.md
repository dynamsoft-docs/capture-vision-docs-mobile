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

The IntermediateResultReceiver class is designed as a standardized way for retrieving intermediate results in image processing workflows in the Dynamsoft Capture Vision architecture.

## Definition

*Assembly:* DynamsoftCore.xcframework

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
| [getObservationParameters](#getobservationparameters) | Gets the observed parameters of the intermediate result receiver. |
| [onTaskResultsReceived](#ontaskresultsreceived) | The callback triggered when task results are received. |
| [onPredetectedRegionsReceived](#onpredetectedregionsreceived) | The callback triggered when pre-detected regions are received. |
| [onLocalizedBarcodesReceived](#onlocalizedbarcodesreceived) | The callback triggered when localized barcodes are received. |
| [onDecodedBarcodesReceived](#ondecodedbarcodesreceived) | The callback triggered when decoded barcodes are received. |
| [onLocalizedTextLinesReceived](#onlocalizedtextlinesreceived) | The callback triggered when localized text lines are received. |
| [onRecognizedTextLinesReceived](#onrecognizedtextlinesreceived) | The callback triggered when recognized text lines are received. |
| [onDetectedQuadsReceived](#ondetectedquadsreceived) | The callback triggered when detected quads are received. |
| [onNormalizedImagesReceived](#onnormalizedimagesreceived) | The callback triggered when normalized images are received. |
| [onColourImageUnitReceived](#oncolourimageunitreceived) | The callback triggered when a colour image unit is received. |
| [onScaledDownColourImageUnitReceived](#onscaleddowncolourimageunitreceived) | The callback triggered when a scaled-down colour image unit is received. |
| [onGrayscaleImageUnitReceived](#ongrayscaleimageunitreceived) | The callback triggered when a grayscale image unit is received. |
| [onTransformedGrayscaleImageUnitReceived](#ontransformedgrayscaleimageunitreceived) | The callback triggered when a transformed grayscale image unit is received. |
| [onEnhancedGrayscaleImageUnitReceived](#onenhancedgrayscaleimageunitreceived) | The callback triggered when an enhanced grayscale image unit is received. |
| [onBinaryImageUnitReceived](#onbinaryimageunitreceived) | The callback triggered when a binary image unit is received. |
| [onTextureDetectionResultUnitReceived](#ontexturedetectionresultunitreceived) | The callback triggered when a texture detection result unit is received. |
| [onTextureRemovedGrayscaleImageUnitReceived](#ontextureremovedgrayscaleimageunitreceived) | The callback triggered when a texture-removed grayscale image unit is received. |
| [onTextureRemovedBinaryImageUnitReceived](#ontextureremovedbinaryimageunitreceived) | The callback triggered when a texture-removed binary image unit is received. |
| [onContoursUnitReceived](#oncontoursunitreceived) | The callback triggered when a contours unit is received. |
| [onLineSegmentsUnitReceived](#onlinesegmentsunitreceived) | The callback triggered when a line segments unit is received. |
| [onTextZonesUnitReceived](#ontextzonesunitreceived) | The callback triggered when a text zones unit is received. |
| [onTextRemovedBinaryImageUnitReceived](#ontextremovedbinaryimageunitreceived) | The callback triggered when a text-removed binary image unit is received. |
| [onShortLinesUnitReceived](#onshortlinesunitreceived) | The callback triggered when a short lines unit is received. |
| [onLogicLinesUnitReceived](#onlogiclinesunitreceived) | The callback triggered when a logic lines unit is received. |
| [onLongLinesUnitReceived](#onlonglinesunitreceived) | The callback triggered when a long lines unit is received. |
| [onCornersUnitReceived](#oncornersunitreceived) | The callback triggered when a corners unit is received. |
| [onCandidateQuadEdgesUnitReceived](#oncandidatequadedgesunitreceived) | The callback triggered when a candidate quad edges unit are detected. |
| [onCandidateBarcodeZonesUnitReceived](#oncandidatebarcodezonesunitreceived) | The callback triggered when a candidate barcode zones unit are detected. |
| [onScaledUpBarcodeImageUnitReceived](#onscaledupbarcodeimageunitreceived) | The callback triggered when a scaled-up barcode image unit is received. |
| [onDeformationResistedBarcodeImageUnitReceived](#ondeformationresistedbarcodeimageunitreceived) | The callback triggered when a deformation-resisted barcode image unit is received. |
| [onComplementedBarcodeImageUnitReceived](#oncomplementedbarcodeimageunitreceived) | The callback triggered when a complemented barcode image unit is received. |

### getObservationParameters

Get the observed parameters of the intermediate result receiver.

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

### onTaskResultsReceived

The callback triggered when task results are received.

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

`unit`: The intermediate result from the task, of type `IntermediateResult`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onPredetectedRegionsReceived

The callback triggered when pre-detected regions are received.

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

`unit`: The intermediate result that contains the pre-detected regions, of type `PredetectedRegionsUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLocalizedBarcodesReceived

The callback triggered when localized barcodes are received.

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

`unit`: The intermediate result that contains the localized barcodes, of type `LocalizedBarcodesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDecodedBarcodesReceived

The callback triggered when decoded barcodes are received.

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

`unit`: The intermediate result that contains the decoded barcodes, of type `DecodedBarcodesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLocalizedTextLinesReceived

The callback triggered when localized text lines are received.

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

`unit`: The intermediate result that contains the localized text lines, of type `LocalizedTextLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onRecognizedTextLinesReceived

The callback triggered when recognized text lines are received.

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

`unit`: The intermediate result that contains the recognized text lines, of type `RecognizedTextLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDetectedQuadsReceived

The callback triggered when detected quads are received.

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

`unit`: The intermediate result that contains the detected quads, of type `DetectedQuadsUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onNormalizedImagesReceived

The callback triggered when normalized images are received.

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

`unit`: The intermediate result that contains the normalized images, of type `NormalizedImagesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onColourImageUnitReceived

The callback triggered when colour images are received.

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

`unit`: The intermediate result that contains the colour images, of type `ColourImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onScaledDownColourImageUnitReceived

The callback triggered when scaled-down colour images are received.

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

`unit`: The intermediate result that contains the scaled-down colour images, of type `ScaledDownColourImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onGrayscaleImageUnitReceived

The callback triggered when grayscale images are received.

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

`unit`: The intermediate result that contains the grayscale images, of type `GrayscaleImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTransformedGrayscaleImageUnitReceived

The callback triggered when transformed grayscale images are received.

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

`unit`: The intermediate result that contains the transformed grayscale images, of type `TransformedGrayscaleImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onEnhancedGrayscaleImageUnitReceived

The callback triggered when enhanced grayscale images are received.

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

`unit`: The intermediate result that contains the enhanced grayscale images, of type `EnhancedGrayscaleImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onBinaryImageUnitReceived

The callback triggered when binary images are received.

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

`unit`: The intermediate result that contains the binary images, of type `BinaryImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextureDetectionResultUnitReceived

The callback triggered when texture detection results are received.

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

`unit`: The intermediate result that contains the texture detection results, of type `TextureDetectionResultUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextureRemovedGrayscaleImageUnitReceived

The callback triggered when texture removed grayscale images are received.

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

`unit`: The intermediate result that contains the texture removed grayscale images, of type `TextureRemovedGrayscaleImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextureRemovedBinaryImageUnitReceived

The callback triggered when texture removed binary images are received.

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

`unit`: The intermediate result that contains the texture removed binary images, of type `TextureRemovedBinaryImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onContoursUnitReceived

The callback triggered when contours are received.

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

`unit`: The intermediate result that contains the contours, of type `ContoursUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onShortLinesUnitReceived

The callback triggered when short lines are received.

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

`unit`: The intermediate result that contains the short lines, of type `DSShortLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLineSegmentsUnitReceived

The callback triggered when line segments are received.

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

`unit`: The intermediate result that contains the line segments, of type `LineSegmentsUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextZonesUnitReceived

The callback triggered when text zones are received.

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

`unit`: The intermediate result that contains the text zones, of type `TextZonesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onTextRemovedBinaryImageUnitReceived

The callback triggered when text removed binary images are received.

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

`unit`: The intermediate result that contains the text removed binary images, of type `TextRemovedBinaryImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLogicLinesUnitReceived

The callback triggered when logic lines are received.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)onLogicLinesUnitReceived:(LogicLinesUnit *)unit
                          info:(DSIntermediateResultExtraInfo *)info
```
2. 
```swift
func onLogicLinesUnitReceived(_ unit: LogicLinesUnit, info: IntermediateResultExtraInfo)
```

**Parameters**

`unit`: The intermediate result that contains the logic lines, of type `LogicLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onLongLinesUnitReceived

The callback triggered when long lines are received.

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

`unit`: The intermediate result that contains the long lines, of type `LongLinesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onCornersUnitReceived

The callback triggered when corners are received.

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

`unit`: The intermediate result that contains the corners, of type `CornersUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onCandidateQuadEdgesUnitReceived

The callback triggered when candidate quad edges are received.

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

`unit`: The intermediate result that contains the candidate quad edges, of type `CandidateQuadEdgesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onCandidateBarcodeZonesUnitReceived

The callback triggered when candidate barcode zones are received.

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

`unit`: The intermediate result that contains the candidate barcode zones, of type `CandidateBarcodeZonesUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onScaledUpBarcodeImageUnitReceived

The callback triggered when scaled up barcode images are received.

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

`unit`: The intermediate result that contains the scaled up barcode images, of type `ScaledUpBarcodeImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onDeformationResistedBarcodeImageUnitReceived

The callback triggered when deformation resisted barcode images are received.

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

`unit`: The intermediate result that contains the deformation resisted barcode images, of type `DeformationResistedBarcodeImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.

### onComplementedBarcodeImageUnitReceived

The callback triggered when complemented barcode images are received.

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

`unit`: The intermediate result that contains the complemented barcode images, of type `ComplementedBarcodeImageUnit`.

`info`: Additional information about the result, of type `IntermediateResultExtraInfo`.
