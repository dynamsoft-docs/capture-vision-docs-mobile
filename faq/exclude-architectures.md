---
layout: default-layout
title: How to fix building errors related to IOS archetecture?
keywords: Dynamsoft Barcode Reader, FAQ, IOS, Mobile, building error, archetecture, arm64
description: How to fix building errors related to IOS archetecture?
needAutoGenerateSidebar: false
---

## How to Solve "Building for iOS Simulator, but linking in dylib built for iOS"

[<< Back to FAQ index](index.md)

Dynamsoft framework can be used to build an app for arm64 iOS. If you build the app for arm64 simulator and you are migrate your app from older versions to Xcode 12 or higher, the following error message may pops up:  

> ld: "Building for iOS Simulator, but linking in dylib built for iOS, file '/ios/Pods/DynamsoftBarcodeReader/DynamsoftBarcodeReader.framework/DynamsoftBarcodeReader' for architecture arm64"  

<br />

**To fix the error:**  

1. Set *Build Settings* > *Build Options* > *VALIDATE_WORKSPACE* to "YES" and then rebuild your project  
2. Set *Build Settings* > *Archetectures* > *Build Active Architecture Only* to "YES" and choose iPhone device run  
3. Set *Build Settings* >  *Architectures* -> $(ARCHS_STANDARD)  

<br />

**If the error message still exists, please make one of the following changes:**  

Switch from framework to xcframeworks  

Or  

Excluded Architectures -> Debug -> Any iPhone simulator -> arm64  

Or  

```ruby
Podfile:
post_install do |installer|
  installer.pods_project.build_configurations.each do |config|
    config.build_settings["EXCLUDED_ARCHS[sdk=iphonesimulator*]"] = "arm64"
  end
end
```

Or  

```ruby
post_install do |installer|
  installer.pods_project.build_configurations.each do |config|
    config.build_settings["EXCLUDED_ARCHS[sdk=iphonesimulator*]"] = "uname -m"
  end
end
```

Or  

```ruby
podspec:
s.pod_target_xcconfig = { 'EXCLUDED_ARCHS[sdk=iphonesimulator*]' => 'arm64' }
s.user_target_xcconfig = { 'EXCLUDED_ARCHS[sdk=iphonesimulator*]' => 'arm64' }
```
