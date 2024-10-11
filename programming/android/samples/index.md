---
layout: default-layout
title: Demo & Samples - Dynamsoft Capture Vision Android Edition
description: The index of Dynamsoft Capture Vision Android demo & samples.
keywords: demo, sample, index, Android
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Demo & Samples

- [Demo \& Samples](#demo--samples)
	- [Demos](#demos)
		- [Barcode Scanner Demo](#barcode-scanner-demo)
	- [Barcode Decoding Samples](#barcode-decoding-samples)
		- [Read Single Barcode (With CameraEnhancer)](#read-single-barcode-with-cameraenhancer)
		- [Read Single Barcode (With CameraX)](#read-single-barcode-with-camerax)
		- [Decode Barcodes from an Image](#decode-barcodes-from-an-image)
		- [Decode Multiple Barcodes from Video Stream](#decode-multiple-barcodes-from-video-stream)
		- [General Barcode Decoding Settings](#general-barcode-decoding-settings)
		- [Barcode Decoding Performance Settings](#barcode-decoding-performance-settings)
		- [Decode Tiny Barcodes](#decode-tiny-barcodes)
		- [Locate an Item with Barcode](#locate-an-item-with-barcode)
	- [ID Scanning Samples](#id-scanning-samples)
		- [Scan a passport or an ID card (via MRZ)](#scan-a-passport-or-an-id-card-via-mrz)
		- [Scan a Driver's License (via PDF417 Barcode)](#scan-a-drivers-license-via-pdf417-barcode)
	- [Document Scanner Samples](#document-scanner-samples)
		- [Scan a Document Page and Deskew automatically](#scan-a-document-page-and-deskew-automatically)
		- [Scan, Edit and Deskew a Document Page](#scan-edit-and-deskew-a-document-page)
	- [Other Use Case Samples](#other-use-case-samples)
		- [Scan VIN Barcode or Text](#scan-vin-barcode-or-text)

## Demos

### Barcode Scanner Demo

  - [View in Google Play Store](https://play.google.com/store/apps/details?id=com.dynamsoft.demo.dynamsoftbarcodereaderdemo&pli=1){:target="_blank"}
  - [Download APK](https://download2.dynamsoft.com/dbr/android/DynamsoftBarcodeReaderDemoAndroid.apk)

<!-- ### MRZ Scanner Demo

  - [View in Google Play Store](https://play.google.com/store/apps/details?id=com.dynamsoft.demo.mrzscannerdemo&pli=1){:target="_blank"}
  - [Download APK](https://download2.dynamsoft.com/dbr/android/DynamsoftMRZScannerDemoAndroid.apk) -->

## Barcode Decoding Samples

### Read Single Barcode (With CameraEnhancer)

Decode barcodes from video streaming. It shows the simplest code to implement a video barcode scanner.

[Check code on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/HelloWorld){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/f57e065a-2155-458b-b3aa-3a5ca2c63573">
</video>

### Read Single Barcode (With CameraX)

Generally the same as `DecodeWithCameraEnhancer` but using `CameraX` library as the input.

[Check code on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/HelloWorld){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/159ddfcf-7885-495e-bc57-52511a66ae1d">
</video>

### Decode Barcodes from an Image

Decode barcodes from an still image. It shows how to select a image from the album and decode it.

[Check code on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/HelloWorld){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/9f302f01-76aa-41e0-b075-662ecde3de17">
</video>

### Decode Multiple Barcodes from Video Stream

This sample shows how to efficiently decode multiple barcodes from the video stream.

[Check code on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/DecodeMultipleBarcodes){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/d1ec55c7-7123-4975-ba22-658cc701c9b6">
</video>

### General Barcode Decoding Settings

Displays general barcode decoding settings and camera settings like barcode formats, expected barcode count and scan region settings. The default scan mode is continuous scanning.

[Check code on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/GeneralSettings){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/99a18a5e-5b2e-4129-9231-bb2d693fd6ea">
</video>

### Barcode Decoding Performance Settings

Parameter configuration guide on improving the speed, read-rate and accuracy of barcode reading. The sample includes the code of image decoding from the album.

[Check code on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/PerformanceSettings){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/823d7f99-7a6a-415a-9b25-f9de4efdc904">
</video>

### Decode Tiny Barcodes

The sample to tell you how to process the tiny barcodes including zoom and focus control.

[Check code on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/UseCase){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/4f226bc1-f5a3-4e35-9674-be13f584ee24">
</video>

### Locate an Item with Barcode

Input an ID with barcode text and detect it from multiple barcodes under the screen.

[Check code on GitHub](https://github.com/Dynamsoft/barcode-reader-mobile-samples/tree/main/android/UseCase){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/8fb7e24a-ba5a-4677-8532-4cde20868504">
</video>

## ID Scanning Samples

### Scan a passport or an ID card (via MRZ)

Scan the MRZ code of a passport or an ID card and parse the information.

[Check code on GitHub](https://github.com/Dynamsoft/mrz-scanner-mobile/tree/main/android/MRZScanner){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/9e967311-10d5-4ea0-90ad-705b423037ff">
</video>

### Scan a Driver's License (via PDF417 Barcode)

Scan the PDF417 barcodes on a drivers' license and extract the drivers information.

[Check code on GitHub](https://github.com/Dynamsoft/capture-vision-mobile-samples/tree/main/Android/DriversLicenseScanner){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/29299e71-936f-4f9b-94ce-d3857d393f3b">
</video>

## Document Scanner Samples

### Scan a Document Page and Deskew automatically

Scan a document page and normalize it automatically.

[Check code on GitHub](https://github.com/Dynamsoft/capture-vision-mobile-samples/tree/main/Android/DocumentScanner){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/075a851c-7802-48bd-a194-a55e5669bd1e">
</video>

### Scan, Edit and Deskew a Document Page

Scan a document page. Edit the boundary and normalize it.

[Check code on GitHub](https://github.com/Dynamsoft/capture-vision-mobile-samples/tree/main/Android/DocumentScanner){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/e487807c-fa13-4779-a7fc-d99ea633cd5f">
</video>

## Other Use Case Samples

### Scan VIN Barcode or Text

Scan the vin barcode or text and extract the vehicle information.

[Check code on GitHub](https://github.com/Dynamsoft/capture-vision-mobile-samples/tree/main/Android/VINScanner){:target="_blank"}

<video controls width="250" autoplay="false">
    <source src="https://github.com/user-attachments/assets/0d1e2cfe-7f6a-4992-b984-81ddaa1d271a">
</video>