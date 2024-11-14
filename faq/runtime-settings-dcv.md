---
layout: default-layout
title: Are all the runtime settings included in the Barcode Reader module of the DCV packages?
keywords: Dynamsoft Barcode Reader, FAQ, Mobile, tech basic, ios, android, dcv, runtime settings
description: Are all the runtime settings included in the Barcode Reader module of the DCV packages?
needAutoGenerateSidebar: false
noTitleIndex: true
breadcrumbText: Runtime Settings
---

# Are all the runtime settings included in the Barcode Reader module of the DCV packages?

[<< Back to FAQ index](index.md)

At the moment, the available runtime settings for the Barcode Reader module in DCV (all editions) are limited to the core ones, namely: *barcodeFormatIds*, *barcodeFormatIds_2*, *expectedBarcodeCount*, and *timeout*. 

The only current exception is the Flutter edition which has *minBarcodeTextLength* and *minResultConfidence* on top of the ones mentioned above.

For reference, here is the [DBRRuntimeSettings](https://www.dynamsoft.com/capture-vision/docs-archive/mobile/programming/react-native/api-reference/interface-dbr-runtime-settings.html?ver=latest) page of the React Native edition of DCV.

The team is working to extend the runtime settings available in all editions of DCV to match the ones available in the regular editions of the Barcode Reader SDK.