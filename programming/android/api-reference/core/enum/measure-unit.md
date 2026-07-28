---
layout: default-layout
title: MeasureUnit - Dynamsoft Capture Vision Android Enumerations
description: The enumeration MeasureUnit of Dynamsoft Capture Vision Android edition describes the unit of measurement for a value.
keywords: measure unit, pixel, percentage
codeAutoHeight: true
---

# Enumeration MeasureUnit

`MeasureUnit` describes the unit of measurement for a value.

```java
public @interface EnumMeasureUnit
{
   /**The value is an absolute pixel count.*/
   public static final int MU_PIXEL = 0;
   /**The value is a percentage of the reference dimension (e.g. 25 = 25%).*/
   public static final int MU_PERCENTAGE = 1;
}
```
