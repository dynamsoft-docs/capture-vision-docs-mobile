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

Dynamsoft Capture Vision (DCV) is an SDK that integrates the key features of Dynamsoft Barcode Reader (DBR), Dynamsoft Label Recognizer (DLR) and Dynamsoft Document Normalizer (DDN) for cross-platform development.

## Key Features

### Barcode Decoding

- Supports all common barcode symbologies.
- Quick access to basic barcode decoding settings.
- Advanced parameter settings are available.

### Document Scanning

<a href = "https://www.dynamsoft.com/label-recognition/overview/" target="_blank">`DynamsoftDocumentNormalizer`</a> is the library designed to detect quads such as document/table boundaries, etc. from images, and perform document normalization on the images in the detected quads. The detectable areas include but are not limited to:

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

In addition, UI configuration APIs are available to

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
