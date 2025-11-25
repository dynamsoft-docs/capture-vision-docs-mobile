---
layout: default-layout
title: EnumValidationStatus - Dynamsoft Barcode Reader Flutter
description: Enumeration EnumValidationStatus of DBR Flutter Edition defines the status of a field's value after the internal validation checks
keywords: captured result, flutter, capture vision, mapping, code parser, validation
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: EnumValidationStatus
---

# EnumValidationStatus

`EnumValidationStatus` is an enumeration that represents whether the associated field's value passed the internal validation checks.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
enum EnumValidationStatus {
    none,
    succeeded,
    failed
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `none` | No validation check has been performed. |
| `succeeded` | The validation of this field was successful. |
| `failed` | The validation of this field was unsuccessful. |
