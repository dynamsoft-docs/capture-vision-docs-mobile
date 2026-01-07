---
layout: default-layout
title: CaptureState - Dynamsoft Capture Vision Android Enumerations
description: The enumeration CaptureState of Dynamsoft Capture Vision Android describes the state of data capturing.
keywords: Capture state
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CaptureState
---

# Enumeration CaptureState

`CaptureState` describes the state of data capturing.

```java
@Retention(SOURCE)
@IntDef({CS_STARTED, CS_STOPPED, CS_PAUSED, CS_RESUME})
public @interface EnumCaptureState
{
   /** The data capturing is started. */
   public static final int CS_STARTED = 0;
   /** The data capturing is stopped. */
   public static final int CS_STOPPED = 1;
   /** The data capturing is paused. */
   public static final int CS_PAUSED = 2;
   /** The data capturing is resumed. */
   public static final int CS_RESUME = 3;
}
```
