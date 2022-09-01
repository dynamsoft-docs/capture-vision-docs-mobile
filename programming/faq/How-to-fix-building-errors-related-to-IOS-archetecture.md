---
layout: default-layout
title: How to fix building errors related to IOS archetecture?
keywords: Dynamsoft Barcode Reader, FAQ, IOS, Mobile, building error, archetecture, arm64
description: How to fix building errors related to IOS archetecture?
needAutoGenerateSidebar: false
---

## How to fix building errors related to IOS archetecture?

[<< Back to FAQ index](index.md)

Dynamsoft framework can be used to build an app for arm64 iOS. If you build the app for arm64 simulator, the following error message may pop up:
> Note -If you migrate your app from old versions to Xcode 12 or higher, the error message is likely to pop up.

<span style="color:red">"Building for iOS Simulator, but linking in dylib built for iOS, file '/ios/Pods/DynamsoftBarcodeReader/DynamsoftBarcodeReader.framework/DynamsoftBarcodeReader' for architecture arm64"</span>


To fix the error:

1. Set Build Settings > Build Options > VALIDATE_WORKSPACE to "YES" and then rebuild your project
2. Set Build Settings > Archetectures > Build Active Architecture Only to YES and choose iPhone device run
3. Set Build Settings > Archetectures > Architectures -> $(ARCHS_STANDARD)

If the error message still exists, please make one of the following changes:

Switch from framework to xcframeworks

Or

Excluded Architectures -> Debug -> Any iPhone simulator -> arm64

Or

```
    Podfile:
    post_install do |installer|
      installer.pods_project.build_configurations.each do |config|
        config.build_settings["EXCLUDED_ARCHS[sdk=iphonesimulator*]"] = "arm64"
      end
    end
```
Or

```
    post_install do |installer|
      installer.pods_project.build_configurations.each do |config|
        config.build_settings["EXCLUDED_ARCHS[sdk=iphonesimulator*]"] = "uname -m"
      end
    end
```
Or
 
```
    podspec:
    s.pod_target_xcconfig = { 'EXCLUDED_ARCHS[sdk=iphonesimulator*]' => 'arm64' }
    s.user_target_xcconfig = { 'EXCLUDED_ARCHS[sdk=iphonesimulator*]' => 'arm64' }
```