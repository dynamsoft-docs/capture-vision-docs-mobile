
# How to Prevent Project Build Failure after Shrinking Code?

This page provides you a possible solution when your project build fails after implementing the code obfuscation.

Generally, you don’t have to add any configurations when shrinking your code because proguard rule is already configured in the aar.

```bash
-keepclasseswithmembernames class * {    
    native <methods>; 
}
-keep class com.dynamsoft.dbr.** { *; }
-keep class com.dynamsoft.dce.** { *; }
```
