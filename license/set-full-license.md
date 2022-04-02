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

# How to Set the License

## Activate the License

## Set the License in the Code

```js
try {
  await DynamsoftBarcodeReader.initLicense("Put-Your-License-Here")
} catch (e) {
  // Catch and log the error message when license activation is failed.
  console.log(e.code)
}
```
