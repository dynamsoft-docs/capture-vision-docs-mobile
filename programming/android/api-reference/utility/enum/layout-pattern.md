---
layout: default-layout
title: LayoutPattern - Dynamsoft Capture Vision Android Enumerations
description: The enumeration LayoutPattern of Dynamsoft Capture Vision Android edition describes the layout pattern for quadrilateral analysis.
keywords: layout pattern
codeAutoHeight: true
---

# Enumeration LayoutPattern

`LayoutPattern` describes the layout pattern for quadrilateral analysis.

```java
public @interface EnumLayoutPattern
{
   /**Algorithm automatically detects the best layout pattern.*/
   public static final int LP_UNKNOWN = 0;
   /**Elements are organized into sequential lines (rows or columns).*/
   public static final int LP_LINES = 1;
   /**Elements are organized into a strict grid/matrix structure.*/
   public static final int LP_MATRIX = 2;
}
```
