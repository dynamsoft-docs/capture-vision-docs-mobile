---
layout: default-layout
title: Class DBRRuntimeSettings of Dynamsoft Capture Vision Xamarin Edition
description: The class of DBR runtime settings
keywords: Class DBRRuntimeSettings, API reference
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: DBRRuntimeSettings
---

# DBRRuntimeSettings

Class `DBRRuntimeSettings`. It stores the basic barcode decoding settings when using Dynamsoft Barcode Reader.

```c#
namespace DCVXamarin
{
    public class DBRRuntimeSettings
    {
        // Sets the formats of the barcode in BarcodeFormat group 1 to be read. Barcode formats in BarcodeFormat group 1 can be combined.
        public EnumBarcodeFormat BarcodeFormatIds { get; set; }

        // Sets the formats of the barcode in BarcodeFormat group 2 to be read. Barcode formats in BarcodeFormat group 1 can be combined.
        public EnumBarcodeFormat_2 BarcodeFormatIds_2 { get; set; }

        // Sets the number of barcodes expected to be detected for each image.
        public int ExpectedBarcodeCount { get; set; }

        // Sets the maximum amount of time (in milliseconds) that should be spent searching for a barcode per page.
        public int Timeout { get; set; }
    }
}
```

## Related API(s)

- [`updateRuntimeSettings`](barcode-reader.md#updateruntimesettingsdbrruntimesettings)
- [`EnumBarcodeFormat`](enum-barcode-format.md)
- [`EnumBarcodeFormat_2`](enum-barcode-format2.md)
