---
layout: default-layout
title: CoreModule - Dynamsoft Core Module Android Edition API Reference
description: The class CoreModule of Dynamsoft Core Module defines general functions of the core module.
keywords: core module, Java, Kotlin
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# CoreModule

The `CoreModule` class defines general functions of the core module.

## Definition

*Namespace:* com.dynamsoft.core.basic_structures

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class CoreModule
```

## Methods

| Method | Description |
| ------ |-------------|
| [`getVersion`](#getversion) | Get the version of the `DynamsoftCore` module. |
| [`enableLogging`](#enablelogging) | Enable the output of logs. |
| [`disableLogging`](#disablelogging) | Disable the output of logs. |

## getVersion

Get the version of the `DynamsoftCore` module.

```java
static String getVersion();
```

**Return Value**

The version of the `DynamsoftCore` module.

### enableLogging

Enable the output of logs.

```java
static void enableLogging(int logMode);
```

**Parameters**

`logMode`: One of the [`EnumLogMode`]({{ site.dcv_enumerations }}core/log-mode.html?lang=android) value.

### disableLogging

Disable the output of logs.

```java
static void disableLogging();
```
