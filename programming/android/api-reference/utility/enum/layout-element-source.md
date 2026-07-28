---
layout: default-layout
title: LayoutElementSource - Dynamsoft Capture Vision Android Enumerations
description: The enumeration LayoutElementSource of Dynamsoft Capture Vision Android edition describes the origin of a layout element.
keywords: layout element source
codeAutoHeight: true
---

# Enumeration LayoutElementSource

`LayoutElementSource` describes the origin of a layout element.

```java
public @interface EnumLayoutElementSource
{
   /**No element exists at this logical grid position.*/
   public static final int LES_NONE = 0;
   /**Element is provided from the original input array.*/
   public static final int LES_INPUT = 1;
   /**Element is reconstructed or filled in by the algorithm.*/
   public static final int LES_INFERRED = 2;
}
```
