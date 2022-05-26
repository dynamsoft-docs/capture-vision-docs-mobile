---
layout: default-layout
title: Dynamsoft Capture Vision - Introduction
description: This is the Introduction Page of Dynamsoft Capture Vision.
keywords:  Capture Vision, Introduction
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: false
breadcrumbText: Introduction
---

# Introduction to Dynamsoft Capture Vision

Dynamsoft Capture Vision (DCV) is an SDK designed for users to quickly embed barcode decoding, document scanning and label text recognizing features to a cross-platform application. A build-in camera view is available for users to capture and display the video streaming for image processing.

## Key Features

### Barcode Decoding

DCV enables users to scan barcodes from static images or video streaming.

#### High Coverage on Barcode Symbologies

The supported barcode symbologies cover the majority of industries such as retail, commodity, drivers' license, etc.

#### Performance

- Speed: DCV is able to scan 500+ barcodes per minutes.
- Read Rate: DCV can easily recognize the barcode even if they are curved, wrinkled, incompleted. The challenging environments like dark, shadowed or glaring can also be overcome.
- Accuracy: The decoded barcode results are evaluated and filtered before output. Users can add additional filter conditions to make the output result even more accurate.

### Document Scanning

DCV can detect quad areas such as the boundaries of document pages and tables from images, and perform document normalization on the images in the detected quads. The detectable areas include but are not limited to:

- Document pages
- Tables
- Cards like ID cards

The normalization process includes:

- Boundary cropping
- Deskew processing

The following attributes of the output image can be adjusted:

- Colour mode
- Contrast
- Brightness

### Label Recognizing

The label recognizing feature of DCV is designed to extract text areas from an image and recognize the extracted characters. Different from the traditional OCR, DLR algorithm is specified on the symbolized text areas such as:

- Price tags
- Inventory labels
- VIN code
- Driver license
- Passport or Visa MRZ
- ID cards

Models, modes and templates are available to improve the recognition rate.

## SDK Modules

### DynamsoftCameraView

`DynamsoftCameraView` is the module that enable users to quickly deploy a camera view to capture and display the video streaming.

### DynamsoftBarcodeReader

`DynamsoftBarcodeReader` is the module that supports barcode decoding feature. Users can specify barcode formats, control the start/stop of the barcode decoding thread, obtain barcode decoding results or upload advanced parameter controls via the module.

### DynamsoftDocumentNormalizer

> Note:
>
> DynamsoftDocumentNormalizer module is not available in v1.0 release.

`DynamsoftDocumentNormalizer` is the module that supports document scanning feature. The module includes the boundary detection algorithm and APIs that enable users to configure detection and normalization settings or upload advanced parameter settings.

### DynamsoftLabelRecognizer

> Note:
>
> DynamsoftLabelRecognizer module is not available in v1.0 release.

`DynamsoftLabelRecognizer` is the module that supports the label text recognition feature. When working with `DynamsoftLabelRecognizer`, users can improve the performance on localizating the text area or recognizing text by switching the recognition modes, modules and templates.

## Programming

- React Native
  - [Getting Started with barcode decoding](programming/react-native/user-guide/barcode-reader.md).
- Flutter (Coming soon)
