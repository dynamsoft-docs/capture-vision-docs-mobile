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

Powered by <a href = "https://www.dynamsoft.com/label-recognition/overview/" target="_blank">`DynamsoftLabelRecognizer`</a> algorithm, DCV is able to extract text areas from an image and recognize the extracted characters. Different from the traditional OCR, DLR algorithm is specified on the symbolized text areas such as:

- Price tags
- Inventory labels
- VIN code
- Driver license
- Passport or Visa MRZ
- ID cards

Models, modes and templates are available to improve the recognition rate.

## SDK Modules

| Module | Introduction |
| ------ | ------------ |
| `DynamsoftCameraView` | This module intergates the features of <a href = "https://www.dynamsoft.com/camera-enhancer/docs/introduction/" target="_blank">`DynamsoftCameraEnhancer`</a>. It helps you to quickly deploy a camera module for video capture. |
| `DynamsoftBarcodeReader` | This module intergates the main features of <a href = "https://www.dynamsoft.com/barcode-reader/overview/" target="_blank">`DynamsoftBarcodeReader`</a>. You can use this module to read barcodes from image or video streaming. |
| `DynamsoftLabelRecognizer` | This module intergates the main features of <a href = "https://www.dynamsoft.com/label-recognition/overview/" target="_blank">`DynamsoftLabelRecognizer`</a>. You can use this module to recognize text from labels. (Currently not supported) |

## Programming

- React Native
  - [Getting Started with barcode decoding](programming/react-native/user-guide/barcode-reader.md).
- Flutter (Coming soon)