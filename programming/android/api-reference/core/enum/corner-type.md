---
layout: default-layout
title: CornerType - Dynamsoft Core Enumerations
description: The enumeration CornerType of Dynamsoft Core describes how the corner is formed by its sides.
keywords: Corner type
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CornerType
codeAutoHeight: true
---

# Enumeration CornerType

`CornerType` categorizes the nature of a corner based on the intersection of its adjoining sides.

```java
@Retention(RetentionPolicy.CLASS)
public @interface EnumCornerType
{
   /** The corner is formed by two intersecting line segments. */
   public static final int CT_NORMAL_INTERSECTED = 0;
   /** The corner is formed by two T intersecting line segments. */
   public static final int CT_T_INTERSECTED = 1;
   /** The corner is formed by two cross intersecting line segments. */
   public static final int CT_CROSS_INTERSECTED = 2;
   /** The two line segments are not intersected but they definitely consist a corner. */
   public static final int CT_NOT_INTERSECTED = 3;
}
```
