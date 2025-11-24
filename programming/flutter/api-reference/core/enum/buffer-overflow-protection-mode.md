---
layout: default-layout
title: BufferOverflowProtectionMode - Dynamsoft Capture Vision Flutter
description: The enumeration BufferOverflowProtectionMode of Dynamsoft Capture Vision Flutter describes the protection modes when the buffer of ImageSourceAdapter is overflow.
keywords: Buffer overflow protection mode 
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BufferOverflowProtectionMode
codeAutoHeight: true
---

# Enumeration BufferOverflowProtectionMode

`BufferOverflowProtectionMode` describes the protection modes to manage situations when the `ImageSourceAdapter`'s buffer exceeds its capacity. 

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
enum EnumBufferOverflowProtectionMode {
  block,
  update
}
```

## Members

| Member | Description |
| ------ | ----------- |
| `block` | New images are blocked when the buffer is full. |
| `update` | New images are appended at the end, and the oldest images are pushed out from the beginning if the buffer is full. |