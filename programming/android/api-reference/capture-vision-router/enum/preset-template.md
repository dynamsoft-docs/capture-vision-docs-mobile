---
layout: default-layout
title: PresetTemplate - Dynamsoft Vision Router Enumerations
description: The enumeration PresetTemplate of Dynamsoft Vision Router describes the preset template.
keywords: Capture state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Enumeration PresetTemplate

`PresetTemplate` describes the preset template names.

## Members

### PT_READ_BARCODES

The default template for the barcode reading tasks.

**Code Snippet**

Specify the preset template in the `startCapturing` method for scanning from the video.

```java
mRouter.startCapturing(EnumPresetTemplate.PT_READ_BARCODES, new CompletionListener() {
    @Override
    public void onSuccess() {}

    @Override
    public void onFailure(int errorCode, String errorString) {}
});
```

Specify the preset template in the `capture` method for reading from an image.

```java
mRouter.capture("Your file path", EnumPresetTemplate.PT_READ_BARCODES);
```

### PT_READ_BARCODES_SPEED_FIRST

The barcode reading template that prioritizes speed over read rate.

### PT_READ_BARCODES_READ_RATE_FIRST

The barcode reading template that prioritizes read rate over speed.

### PT_READ_SINGLE_BARCODE

The barcode reading template that specifically focuses on the single-barcode-scanning scenario.

### PT_RECOGNIZE_TEXT_LINES

The preset template for the text line recognition tasks.

### PT_RECOGNIZE_NUMBERS

The preset template for the number recognition tasks.

### PT_RECOGNIZE_LETTERS

The preset template for the letter recognition tasks.

### PT_RECOGNIZE_NUMBERS_AND_LETTERS

The preset template for the number and letter recognition tasks.

### PT_RECOGNIZE_NUMBERS_AND_UPPERCASE_LETTERS

The preset template for the number and uppercase letter recognition tasks.

### PT_RECOGNIZE_UPPERCASE_LETTERS

The preset template for the uppercase letter recognition tasks.

### PT_DETECT_DOCUMENT_BOUNDARIES

The default template for the document boundary detection.

### PT_DETECT_AND_NORMALIZE_DOCUMENT

The default template for the document detection and normalization.

### PT_NORMALIZE_DOCUMENT

The default template for the document normalization.

### PT_DEFAULT

The default template that performs barcode decoding, label recognizing, boundary detecting and document normalizing. The template name is "Default".
