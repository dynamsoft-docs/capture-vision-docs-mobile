---
layout: default-layout
title: How to Prevent Project Build Failure after Shrinking Code in Xamarin.Forms?
keywords: Dynamsoft Capture Vision, FAQs, Xamarin.Forms
description: How to Prevent Project Build Failure after Shrinking Code in Xamarin.Forms?
needAutoGenerateSidebar: false
noTitleIndex: true
breadcrumbText: Add Proguard
---

# How to Prevent Project Build Failure after Shrinking Code in Xamarin.Forms?

[<< Back to FAQ index](index.md)

This page provides you a possible solution when your project build fails after implementing the code obfuscation.

Generally, you don't have to add any configurations when shrinking your code because ProGuard rules are already configured in the library. If your build still fails after shrinking code, you can try enabling ProGuard in your project and add the following code in your **proguard_xamarin.cfg** file.

```bash
-keepclasseswithmembernames class * {    
    native <methods>; 
}
-keep class com.dynamsoft.dbr.** { *; }
-keep class com.dynamsoft.dce.** { *; }
```

You can view the <a href="https://learn.microsoft.com/en-us/xamarin/android/deploy-test/release-prep/proguard?tabs=macos" target="_blank">official documents</a> for how to enable ProGuard.
