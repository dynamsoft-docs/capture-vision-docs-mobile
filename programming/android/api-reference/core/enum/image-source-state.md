---
layout: default-layout
title: ImageSourceState - Dynamsoft Core Enumerations
description: The enumeration ImageSourceState of Dynamsoft Core describes the state of ImageSourceAdapter.
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
public @interface EnumImageSourceState
{
   /** The buffer of ImageSourceAdapter is temporarily empty. */
   public static final int ISS_BUFFER_EMPTY = 0;
   /** The source of ImageSourceAdapter is empty. */
   public static final int ISS_EXHAUSTED = 1;
}
```
