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

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumIntermediateResultUnitType {
    /** No intermediate result. */
    long IRUT_NULL = 0L;
    /** A scaled full-color image. */
    long IRUT_SCALED_COLOUR_IMAGE = 1L;
    /** A color image that has been scaled down for efficiency. */
    long IRUT_SCALED_DOWN_COLOUR_IMAGE = 1L << 1;
    /** A grayscale image derived from the original input. */
    long IRUT_GRAYSCALE_IMAGE = 1L << 2;
    /** A grayscale image that has undergone transformation. */
    long IRUT_TRANSOFORMED_GRAYSCALE_IMAGE = 1L << 3;
    /** A grayscale image enhanced for further processing. */
    long IRUT_ENHANCED_GRAYSCALE_IMAGE = 1L << 4;
    /** Regions pre-detected as potentially relevant for further analysis. */
    long IRUT_PREDETECTED_REGIONS = 1L << 5;
    /** A binary (black and white) image. */
    long IRUT_BINARY_IMAGE = 1L << 6;
    /** Results from detecting textures within the image. */
    long IRUT_TEXTURE_DETECTION_RESULT = 1L << 7;
    /** A grayscale image with textures removed to enhance subject details like text or barcodes. */
    long IRUT_TEXTURE_REMOVED_GRAYSCALE_IMAGE = 1L << 8;
    /** A binary image with textures removed, useful for clear detection of subjects without background noise. */
    long IRUT_TEXTURE_REMOVED_BINARY_IMAGE = 1L << 9;
    /** Detected contours within the image, which can help in identifying shapes and objects. */
    long IRUT_CONTOURS = 1L << 10;
    /** Detected line segments, useful in structural analysis of the image content. */
    long IRUT_LINE_SEGMENTS = 1L << 11;
    /** Identified text zones, indicating areas with potential textual content. */
    long IRUT_TEXT_ZONES = 1L << 12;
    /** A binary image with text regions removed. */
    long IRUT_TEXT_REMOVED_BINARY_IMAGE = 1L << 13;
    /** Zones identified as potential barcode areas, aiding in focused barcode detection. */
    long IRUT_CANDIDATE_BARCODE_ZONES = 1L << 14;
    /** Barcodes that have been localized but not yet decoded. */
    long IRUT_LOCALIZED_BARCODES = 1L << 15;
    /** Barcode images scaled up or down for improving speed, readability or decoding accuracy. */
    long IRUT_SCALED_BARCODE_IMAGE = 1L << 16;
    /** Images of barcodes processed to resist deformation and improve decoding success. */
    long IRUT_DEFORMATION_RESISTED_BARCODE_IMAGE = 1L << 17;
    /** Barcode images that have been complemented. */
    long IRUT_COMPLEMENTED_BARCODE_IMAGE = 1L << 18;
    /** Successfully decoded barcodes. */
    long IRUT_DECODED_BARCODES = 1L << 19;
    /** Detected long lines. */
    long IRUT_LONG_LINES = 1L << 20;
    /** Detected corners within the image. */
    long IRUT_CORNERS = 1L << 21;
    /** Candidate edges identified as potential components of quadrilaterals. */
    long IRUT_CANDIDATE_QUAD_EDGES = 1L << 22;
    /** Successfully detected quadrilaterals. */
    long IRUT_DETECTED_QUADS = 1L << 23;
    /** Text lines that have been localized in preparation for recognition. */
    long IRUT_LOCALIZED_TEXT_LINES = 1L << 24;
    /** Successfully recognized text lines. */
    long IRUT_RECOGNIZED_TEXT_LINES = 1L << 25;
    /** Successfully deskewed images. */
    long IRUT_DESKEWED_IMAGES = 1L << 26;
    /** Detected short lines. */
    long IRUT_SHORT_LINES = 1L << 27;
    /** Recognized raw text lines. */
    public static final long IRUT_RAW_TEXT_LINES = 1L << 28;
    /**Detected logic lines.*/
    public static final long IRUT_LOGIC_LINES = 1L << 29;
    /**Detected logic lines.*/
    public static final long IRUT_ENHANCED_IMAGE = 1L << 30;
    /** A mask to select all types of intermediate results. */
    long IRUT_ALL = 0xFFFFFFFFFFFFFFFF;
}
```
