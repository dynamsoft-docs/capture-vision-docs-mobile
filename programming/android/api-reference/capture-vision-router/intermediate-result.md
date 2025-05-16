---
layout: default-layout
title: Intermediate Result APIs of CaptureVisionRouter - Dynamsoft Capture Vision Router Module Android Edition API Reference
description: Intermediate Result APIs references of CaptureVisionRouter.
keywords: capture vision, intermediate result, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# Intermediate Result APIs

| Method | Description |
| ------ | ----------- |
| `getIntermediateResultManager` | Returns an object, of type [`IntermediateResultManager`](auxiliary-classes/intermediate-result-manager.md), that manages intermediate results. |

## getIntermediateResultManager

Returns an object, of type [`IntermediateResultManager`](auxiliary-classes/intermediate-result-manager.md), that manages intermediate results.

```java
IntermediateResultManager getIntermediateResultManager();
```

**Return Value**

An object of [`IntermediateResultManager`](auxiliary-classes/intermediate-result-manager.md).

**Code Snippet**

The following code snippet shows how to regisiter a `IntermediateResultReceiver` with the `IntermediateResultManager` and receive the localized barcodes.

```java
IntermediateResultManager intermediateResultManager;
intermediateResultManager = mRouter.getIntermediateResultManager();
intermediateResultManager.addResultReceiver(new IntermediateResultReceiver() {
    @Override
    public void onLocalizedBarcodesReceived(@NonNull LocalizedBarcodesUnit unit, IntermediateResultExtraInfo info) {
        // Add code to do when localized barcodes are received.
    }    
    // You can add multiple callback methods here to monitor different types of intermediate results.
});
```

See also:

- [IntermediateResultManager](auxiliary-classes/intermediate-result-manager.md)
- [IntermediateResultReceiver](auxiliary-classes/intermediate-result-receiver.md)
- [EnumIntermediateResultUnitType]({{ site.dcv_android_api }}core/enum/intermediate-result-unit-type.html?lang=android)
