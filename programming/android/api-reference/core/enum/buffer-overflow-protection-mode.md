---
layout: default-layout
title: BufferOverflowProtectionMode - Dynamsoft Core Enumerations
description: The enumeration BufferOverflowProtectionMode of Dynamsoft Core describes the protection modes when the buffer of ImageSourceAdapter is overflow.
keywords: Buffer overflow protection mode 
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BufferOverflowProtectionMode
codeAutoHeight: true
---

# Enumeration BufferOverflowProtectionMode

`BufferOverflowProtectionMode` describes the protection modes to manage situations when the `ImageSourceAdapter`'s buffer exceeds its capacity. 

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumBufferOverflowProtectionMode
{
   /** New images are blocked when the buffer is full.*/
   int BOPM_BLOCK = 0;
   /** New images are appended at the end, and oldest images are pushed out from the beginning if thebuffer is full.*/
   int BOPM_UPDATE = 1;
}
```
