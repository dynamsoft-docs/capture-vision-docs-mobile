---
layout: default-layout
title: ImageSourceState - Dynamsoft Capture Vision Android Enumerations
description: The enumeration ImageSourceState of Dynamsoft Capture Vision Android describes the state of ImageSourceAdapter.
keywords: Image source state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: ImageSourceState
codeAutoHeight: true
ignore: true
---
<!--Moved from Core to CVR in May 2023-->

# Enumeration ImageSourceState

`ImageSourceState` describes the state of `ImageSourceAdapter`.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumImageSourceAdapterStatus
{
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   int ISAS_BUFFER_EMPTY = 0;
   /** The source of ImageSourceAdapter is empty. */
   int ISAS_EXHAUSTED = 1;
}
```
