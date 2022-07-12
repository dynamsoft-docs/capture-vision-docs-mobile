---
layout: default-layout
title: License Initialization - Dynamsoft Capture Vision
description: This is the License Activation Page of Dynamsoft Capture Vision.
keywords:  Capture Vision, License Activation
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: License Activation
---

# License Initialization

## Get a trial key

- The `BarcodeReader` module of Dynamsoft Capture Vision needs a valid license to work.
- A time-limited public trial license is available for every new device for the first use of Dynamsoft Capture Vision. You can find the public trial license on the following parts of this page.
- If your public trial key is expired, please visit <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=dbr&utm_source=docs" target="_blank">Private Trial License Page</a> to get a 30-day trial extension.

## Get a full license

- [Contact us](https://www.dynamsoft.com/company/contact/)  to purchase a full license

## Initialize the license

The following code snippets are using the public trial license to initialize the license. You can replace the public trial license with your own license key.

Open the **App.js** file. In componentDidMount, add the following code:

<div class="sample-code-prefix"></div>
>- React Native
>- Flutter
>
>1. 
```js
componentDidMount() {
   (async () => {
      try {
         // Here we use a public trial key as an example.
         // The public trial key is time-limited.
         // You can visit https://www.dynamsoft.com/customer/license/trialLicense?utm_source=guide&product=dcv&package=rn to get a private trial license.
         // Contact us for more information about the full license https://www.dynamsoft.com/company/contact/?ver=latest
         await DynamsoftBarcodeReader.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9")
      } catch (e) {
         console.log(e)
      }
   })();
}
```
2. 
```dart
try {
   await DynamsoftBarcodeReader.initLicense(license: 'Put-Your-License-Here');
} catch (e) {
   print('license error = $e');
}
```
