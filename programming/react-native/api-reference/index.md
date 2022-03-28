---
layout: default-layout
title: The index of React Native Dynamsoft Capture Vision API reference
description: This page is the index of React Native API reference
keywords: API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Index
---

# Dynamsoft

## DynamsoftCameraView Class

| Properties | Description |
| ---------- | ----------- |
| [`scanRegion`](camera-view.md#scanregion) | Determines the area of interest. Dynamsoft Capture Vision will not process the other areas when the scan region is specified. |
| [`isScanRegionVisible`](camera-view.md#isscanregionvisible) | Determines whether the scan region is visible. |

## DynamsoftBarcodeReader Class

| Methods | Description |
| ------- | ----------- |
| [`initLicense`](#initlicense) | Initialize the license of Dynamsoft Capture Vision.
 |
| [`createInstance`](#createinstance) | Create a barcode reader instance. |
| [`getVersion`](#getversion) | Get the version of `DynamsoftBarcodeReader`, which is packaged in Dynamsoft Capture Vision. |
| [`getDBRRuntimeSettings`](#getdbrruntimesettings) | Get the current runtime settings of `DynamsoftBarcodeReader`. |
| [`updateDBRRuntimeSettings`](#updatedbrruntimesettings) | Update the runtime settings of `DynamsoftBarcodeReader` with a DBRRuntimeSettings struct or a template. |
| [`resetDBRRuntimeSettings`](#resetdbrruntimesettings) | Reset the runtime settings of `DynamsoftBarcodeReader` to default. |
| [`outputDBRRuntimeSettings`](#outputdbrruntimesettings) | Output the runtime settings of `DynamsoftBarcodeReader` to string. |
| [`startBarcodeScanning`](#startbarcodescanning) | Start the barcode decoding thread. |
| [`stopBarcodeScanning`](#stopbarcodescanning) | Stop the barcode decoding thread. |
| [`addFrameListener`](#addframelistener) | Specifies an event handler that fires after the library finishes scanning a frame. |
