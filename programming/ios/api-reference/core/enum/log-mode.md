---
layout: default-layout
title: LogMode - Dynamsoft Core Enumerations
description: The enumeration LogMode of Dynamsoft Core describes the logging mode of the library.
keywords: logging mode
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: LogMode
codeAutoHeight: true
---

# Enumeration LogMode

`LogMode` describes the logging modes.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSLogMode)
{
    /**
     * Output the log information in the console.
     */
    DSLogModeConsole = 1 << 0,
    /**
     * Output the log information to a log file.
     */
    DSLogModeFile = 1 << 1,
};
```
>
```swift
public enum LogMode : Int
{
   /**
    * Output the log information in the console.
    */
   case console = 1 << 0
   /**
    * Output the log information to a log file.
    */
   case file = 1 << 1
};
```
