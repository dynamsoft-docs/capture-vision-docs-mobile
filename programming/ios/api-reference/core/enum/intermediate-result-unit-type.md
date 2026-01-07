---
layout: default-layout
title: IntermediateResultUnitType - Dynamsoft Capture Vision iOS Enumerations
description: The enumeration IntermediateResultUnitType of Dynamsoft Capture Vision iOS describes the type of the intermediate result unit.
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
    /** A scaled full-color image. */
    DSIntermediateResultUnitTypeScaledColourImage = 1,
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
    /** Barcode images scaled up or down for improving the speed, readability or decoding accuracy. */
    DSIntermediateResultUnitTypeScaledBarcodeImage = 1 << 16,
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
    /** Successfully deskewed images. */
    DSIntermediateResultUnitTypeDeskewedImages = 1 << 26,
    /** Detected short lines. */
    DSIntermediateResultUnitTypeShortLines = 1 << 27,
    /** Recognized raw text lines. */
    DSIntermediateResultUnitTypeRawTextLines = 1 << 28,
    /**Detected logic lines.*/
    DSIntermediateResultUnitTypeLogicLines = 1 << 29,
    /** Successfully enhanced images. */
    DSIntermediateResultUnitTypeEnhancedImages = 1 << 30,
    /** A mask to select all types of intermediate results. */
    DSIntermediateResultUnitTypeAll = 0xFFFFFFFFFFFFFFFF
};
```
>
```swift
struct IntermediateResultUnitType: OptionSet {
   let rawValue: Int
   /** No intermediate result. */
   static let null = IntermediateResultUnitType(rawValue: 0)
   /** A scaled full-color image. */
   static let scaledColourImage = IntermediateResultUnitType(rawValue: 1 << 0)
   /** A color image that has been scaled down for efficiency. */
   static let scaledDownColourImage = IntermediateResultUnitType(rawValue: 1 << 1)
   /** A grayscale image derived from the original input. */
   static let grayscaleImage = IntermediateResultUnitType(rawValue: 1 << 2)
   /** A grayscale image that has undergone transformation. */
   static let transformedGrayscaleImage = IntermediateResultUnitType(rawValue: 1 << 3)
   /** A grayscale image enhanced for further processing. */
   static let enhancedGrayscaleImage = IntermediateResultUnitType(rawValue: 1 << 4)
   /** Regions pre-detected as potentially relevant for further analysis. */
   static let predetectedRegions = IntermediateResultUnitType(rawValue: 1 << 5)
   /** A binary (black and white) image. */
   static let binaryImage = IntermediateResultUnitType(rawValue: 1 << 6)
   /** Results from detecting textures within the image. */
   static let textureDetectionResult = IntermediateResultUnitType(rawValue: 1 << 7)
   /** A grayscale image with textures removed to enhance subject details like text or barcodes. */
   static let textureRemovedGrayscaleImage = IntermediateResultUnitType(rawValue: 1 << 8)
   /** A binary image with textures removed, useful for clear detection of subjects without background noise. */
   static let textureRemovedBinaryImage = IntermediateResultUnitType(rawValue: 1 << 9)
   /** Detected contours within the image, which can help in identifying shapes and objects. */
   static let contours = IntermediateResultUnitType(rawValue: 1 << 10)
   /** Detected line segments, useful in structural analysis of the image content. */
   static let lineSegments = IntermediateResultUnitType(rawValue: 1 << 11)
   /** Identified text zones, indicating areas with potential textual content. */
   static let textZones = IntermediateResultUnitType(rawValue: 1 << 12)
   /** A binary image with text regions removed. */
   static let textRemovedBinaryImage = IntermediateResultUnitType(rawValue: 1 << 13)
   /** Zones identified as potential barcode areas, aiding in focused barcode detection. */
   static let candidateBarcodeZones = IntermediateResultUnitType(rawValue: 1 << 14)
   /** Barcodes that have been localized but not yet decoded. */
   static let localizedBarcodes = IntermediateResultUnitType(rawValue: 1 << 15)
   /** Barcode images scaled up or down for improving speed, readability or decoding accuracy. */
   static let scaledBarcodeImage = IntermediateResultUnitType(rawValue: 1 << 16)
   /** Images of barcodes processed to resist deformation and improve decoding success. */
   static let deformationResistedBarcodeImage = IntermediateResultUnitType(rawValue: 1 << 17)
   /** Barcode images that have been complemented. */
   static let complementedBarcodeImage = IntermediateResultUnitType(rawValue: 1 << 18)
   /** Successfully decoded barcodes. */
   static let decodedBarcodes = IntermediateResultUnitType(rawValue: 1 << 19)
   /** Detected long lines. */
   static let longLines = IntermediateResultUnitType(rawValue: 1 << 20)
   /** Detected corners within the image. */
   static let corners = IntermediateResultUnitType(rawValue: 1 << 21)
   /** Candidate edges identified as potential components of quadrilaterals. */
   static let candidateQuadEdges = IntermediateResultUnitType(rawValue: 1 << 22)
   /** Successfully detected quadrilaterals. */
   static let detectedQuads = IntermediateResultUnitType(rawValue: 1 << 23)
   /** Text lines that have been localized in preparation for recognition. */
   static let localizedTextLines = IntermediateResultUnitType(rawValue: 1 << 24)
   /** Successfully recognized text lines. */
   static let recognizedTextLines = IntermediateResultUnitType(rawValue: 1 << 25)
   /** Successfully deskewed images. */
   static let deskewedImages = IntermediateResultUnitType(rawValue: 1 << 26)
   /** Detected short lines. */
   static let shortLines = IntermediateResultUnitType(rawValue: 1 << 27)
   /** Recognized raw text lines. */
   rawTextLines = IntermediateResultUnitType(rawValue: 1 << 28)
   /**Detected logic lines.*/
   logicLines = IntermediateResultUnitType(rawValue: 1 << 29)
   /** Successfully enhanced images. */
   enhancedImages = IntermediateResultUnitType(rawValue: 1 << 30)
   /** A mask to select all types of intermediate results. */
   static let all = 0xFFFFFFFFFFFFFFFF
}
```
