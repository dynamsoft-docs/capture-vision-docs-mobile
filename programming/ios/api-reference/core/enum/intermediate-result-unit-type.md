---
layout: default-layout
title: IntermediateResultUnitType - Dynamsoft Core Enumerations
description: The enumeration IntermediateResultUnitType of Dynamsoft Core describes the type of the intermediate result unit.
keywords: Intermediate result unit type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: IntermediateResultUnitType
codeAutoHeight: true
---

# Enumeration IntermediateResultUnitType

`IntermediateResultUnitType` defines different types of intermediate results generated or expected to be generated during image processing.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_OPTIONS(NSUInteger, DSIntermediateResultUnitType) {
    /** No intermediate result. */
    DSIntermediateResultUnitTypeNull = 0,
    /** A full-color image. */
    DSIntermediateResultUnitTypeColourImage = 1,
    /** A color image that has been scaled down for efficiency. */
    DSIntermediateResultUnitTypeScaledDownColourImage = 1 << 1,
    /** A grayscale image derived from the original input. */
    DSIntermediateResultUnitTypeGrayscaleImage = 1 << 2,
    /** A grayscale image that has undergone transformation. */
    DSIntermediateResultUnitTypeTransformedGrayscaleImage = 1 << 3,
    /** A grayscale image enhanced for further processing. */
    DSIntermediateResultUnitTypeEnhancedGrayscaleImage = 1 << 4,
    /** Regions pre-detected as potentially relevant for further analysis. */
    DSIntermediateResultUnitTypePredetectedRegions = 1 << 5,
    /** A binary (black and white) image. */
    DSIntermediateResultUnitTypeBinaryImage = 1 << 6,
    /** Results from detecting textures within the image. */
    DSIntermediateResultUnitTypeTextureDetectionResult = 1 << 7,
    /** A grayscale image with textures removed to enhance subject details like text or barcodes. */
    DSIntermediateResultUnitTypeTextureRemovedGrayscaleImage = 1 << 8,
    /** A binary image with textures removed, useful for clear detection of subjects without background noise. */
    DSIntermediateResultUnitTypeTextureRemovedBinaryImage = 1 << 9,
    /** Detected contours within the image, which can help in identifying shapes and objects. */
    DSIntermediateResultUnitTypeContours = 1 << 10,
    /** Detected line segments, useful in structural analysis of the image content. */
    DSIntermediateResultUnitTypeLineSegments = 1 << 11,
    /** Identified text zones, indicating areas with potential textual content. */
    DSIntermediateResultUnitTypeTextZones = 1 << 12,
    /** A binary image with text regions removed. */
    DSIntermediateResultUnitTypeTextRemovedBinaryImage = 1 << 13,
    /** Zones identified as potential barcode areas, aiding in focused barcode detection. */
    DSIntermediateResultUnitTypeCandidateBarcodeZones = 1 << 14,
    /** Barcodes that have been localized but not yet decoded. */
    DSIntermediateResultUnitTypeLocalizedBarcodes = 1 << 15,
    /** Barcode images scaled up for improved readability or decoding accuracy. */
    DSIntermediateResultUnitTypeScaledUpBarcodeImage = 1 << 16,
    /** Images of barcodes processed to resist deformation and improve decoding success. */
    DSIntermediateResultUnitTypeDeformationResistedBarcodeImage = 1 << 17,
    /** Barcode images that have been complemented. */
    DSIntermediateResultUnitTypeComplementedBarcodeImage = 1 << 18,
    /** Successfully decoded barcodes. */
    DSIntermediateResultUnitTypeDecodedBarcodes = 1 << 19,
    /** Detected long lines. */
    DSIntermediateResultUnitTypeLongLines = 1 << 20,
    /** Detected corners within the image. */
    DSIntermediateResultUnitTypeCorners = 1 << 21,
    /** Candidate edges identified as potential components of quadrilaterals. */
    DSIntermediateResultUnitTypeCandidateQuadEdges = 1 << 22,
    /** Successfully detected quadrilaterals. */
    DSIntermediateResultUnitTypeDetectedQuads = 1 << 23,
    /** Text lines that have been localized in preparation for recognition. */
    DSIntermediateResultUnitTypeLocalizedTextLines = 1 << 24,
    /** Successfully recognized text lines. */
    DSIntermediateResultUnitTypeRecognizedTextLines = 1 << 25,
    /** Successfully normalized images. */
    DSIntermediateResultUnitTypeNormalizedImages = 1 << 26,
    /** Detected short lines. */
    DSIntermediateResultUnitTypeShortLines = 1 << 27,
    /** Recognized raw text lines. */
    DSIntermediateResultUnitTypeRawTextLines = 1 << 28,
    /**Detected logic lines.*/
    DSIntermediateResultUnitTypeLogicLines = 1 << 29,
    /** A mask to select all types of intermediate results. */
    DSIntermediateResultUnitTypeAll = 0xFFFFFFFFFFFFFFFF
};
```
>
```swift
public enum IntermediateResultUnitType: Int {
    /** No intermediate result. */
    case null = 0
    /** A full-color image. */
    case colourImage = 1
    /** A color image that has been scaled down for efficiency. */
    case scaledDownColourImage = 1 << 1
    /** A grayscale image derived from the original input. */
    case grayscaleImage = 1 << 2
    /** A grayscale image that has undergone transformation. */
    case transformedGrayscaleImage = 1 << 3
    /** A grayscale image enhanced for further processing. */
    case enhancedGrayscaleImage = 1 << 4
    /** Regions pre-detected as potentially relevant for further analysis. */
    case predetectedRegions = 1 << 5
    /** A binary (black and white) image. */
    case binaryImage = 1 << 6
    /** Results from detecting textures within the image. */
    case textureDetectionResult = 1 << 7
    /** A grayscale image with textures removed to enhance subject details like text or barcodes. */
    case textureRemovedGrayscaleImage = 1 << 8
    /** A binary image with textures removed, useful for clear detection of subjects without background noise. */
    case textureRemovedBinaryImage = 1 << 9
    /** Detected contours within the image, which can help in identifying shapes and objects. */
    case contours = 1 << 10
    /** Detected line segments, useful in structural analysis of the image content. */
    case lineSegments = 1 << 11
    /** Identified text zones, indicating areas with potential textual content. */
    case textZones = 1 << 12
    /** A binary image with text regions removed. */
    case textRemovedBinaryImage = 1 << 13
    /** Zones identified as potential barcode areas, aiding in focused barcode detection. */
    case candidateBarcodeZones = 1 << 14
    /** Barcodes that have been localized but not yet decoded. */
    case localizedBarcodes = 1 << 15
    /** Barcode images scaled up for improved readability or decoding accuracy. */
    case scaledUpBarcodeImage = 1 << 16
    /** Images of barcodes processed to resist deformation and improve decoding success. */
    case deformationResistedBarcodeImage = 1 << 17
    /** Barcode images that have been complemented. */
    case complementedBarcodeImage = 1 << 18
    /** Successfully decoded barcodes. */
    case decodedBarcodes = 1 << 19
    /** Detected long lines. */
    case longLines = 1 << 20
    /** Detected corners within the image. */
    case corners = 1 << 21
    /** Candidate edges identified as potential components of quadrilaterals. */
    case candidateQuadEdges = 1 << 22
    /** Successfully detected quadrilaterals. */
    case detectedQuads = 1 << 23
    /** Text lines that have been localized in preparation for recognition. */
    case localizedTextLines = 1 << 24
    /** Successfully recognized text lines. */
    case recognizedTextLines = 1 << 25
    /** Successfully normalized images. */
    case normalizedImages = 1 << 26
    /** Detected short lines. */
    case shortLines = 1 << 27
    /** Recognized raw text lines. */
    rawTextLines = 1 << 28
    /**Detected logic lines.*/
    logicLines = 1 << 29
    /** A mask to select all types of intermediate results. */
    case all = 0xFFFFFFFFFFFFFFFF
}
```
