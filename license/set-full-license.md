---
layout: default-layout
title: Dynamsoft Capture Vision - Set License
description: This is the License Activation Page of Dynamsoft Capture Vision.
keywords:  Capture Vision, License Activation
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
breadcrumbText: License Activation
---

# How to Activate the License

## Set the License in the Code

Open the **App.js** file. In componentDidMount, add the following code:

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
