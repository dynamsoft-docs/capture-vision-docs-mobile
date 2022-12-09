
# How to Prevent Project Build Failure after Shrinking Code in Xamarin.Forms?

This page provides you a possible solution when your project build fails after implementing the code obfuscation.

Generally, you don’t have to add any configurations when shrinking your code because proguard rule is already configured in the library. If you still build failed after shrinking code, you can try enabling proguard in your project and add the following code in your **proguard_xamarin.cfg** file.

```bash
-keepclasseswithmembernames class * {    
    native <methods>; 
}
-keep class com.dynamsoft.dbr.** { *; }
-keep class com.dynamsoft.dce.** { *; }
```
