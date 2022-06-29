---
layout: default-layout
title: Getting Started with Barcode Reader
description: This page is the user guide of Dynamsoft Capture Vision - Barcode Reader module
keywords: User guide, Barcode Reader
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
breadcrumbText: Guide of Barcode Reader
---

# Dynamsoft Capture Vision - Barcode Reader User Guide

In this guide, we will explore the Barcode Reader module of the Dynamsoft Capture Vision library.

## Table of Contents

- [System Requirements](#system-requirements)
- [Installation](#installation)
- [Build Your Barcode Scanner App](#build-your-barcode-scanner-app)
  - [Initialize the Project](#initialize-the-project)
  - [Include the Library](#include-the-library)
  - [Configure the Barcode Reader](#configure-the-barcode-reader)
  - [Rendering the UI](#rendering-the-ui)
  - [Configure Camera Permissions](#configure-camera-permissions)
  - [Run the Project](#run-the-project)
- [Customizing the Barcode Reader](#customizing-the-barcode-reader)
  - [Using the Settings Templates](#using-the-settings-templates)
  - [Using the DBRRuntimeSettings Interface](#using-the-dbrruntimesettings-interface)
  - [Customizing the Scan Region](#customizing-the-scan-region)
- [Get a License Key](#get-a-license-key)

## System Requirements

### Flutter

### Android

- Supported OS: Android 5.0 (API Level 21) or higher.
- Supported ABI: **armeabi-v7a**, **arm64-v8a**, **x86** and **x86_64**.
- Development Environment: Android Studio 3.4+ (Android Studio 4.2+ recommended).
- JDK: 1.8+

### iOS

- Supported OS: **iOS 10.0** or higher.
- Supported ABI: **arm64** and **x86_64**.
- Development Environment: Xcode 7.1 and above (Xcode 13.0+ recommended), CocoaPods 1.11.0+.

## Installation

In **pubspec.yaml** add the library of `DynamsoftCaptureVision`

```dart
dev_dependencies:    
  dynamsoft_capture_vision_flutter: ^1.0.0
```

Use the following command to add the library to your project:

```bash
flutter pub get
```

## Build Your Barcode Scanner App

Now you will learn how to create a simple barcode scanner using Dynamsoft Capture Vision SDK.

### Initialize the Project

Create a new Flutter project

```bash
flutter create simple_barcode_scanner
```

### Include the Library

View the [installation section](#installation) for how to add the library. In **main.dart** of your project, import the library.

```dart
import 'package:dynamsoft_capture_vision_flutter/dynamsoft_capture_vision_flutter.dart';
```

### License Activation

The barcode reading module of Dynamsoft Capture Vision needs a valid license to work. In the **main()** function, add the following code to activate the license.

```dart
void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  // Put your license here.
  final String licenseKey = '';
  // Initialize the license so that you can use full feature of the Barcode Reader module.
  try {
    await DynamsoftBarcodeReader.initLicense(license: licenseKey);
  } catch (e) {
    print(e);
  }

  runApp(const MyApp());
}
```

### Configure the Barcode Reader

In this section, we are going to work on the **_MyHomePageState** class in the newly created project to add the barcode decoding feature.

Define the following attributes:

```dart
late final DynamsoftBarcodeReader _barcodeReader;
final DynamsoftCameraView _cameraView = DynamsoftCameraView();
List<BarcodeResult> decodeRes = [];
```

- `barcodeReader`: The object that implements barcode decoding feature. Users can configure barcode decoding settings via this object.
- `cameraView`: The camera view that displays the video streaming.
- `decodeResults`: An object that will be used to receive and stores barcode decoding result.

Add in the **initState** add an **async** method to initialize the barcode reader.

```dart
class _MyHomePageState extends State<MyHomePage> {
  @override
  void initState() {
    super.initState();
    _configDBR();
  }

  _configDBR() async {

    /// Create an instance of barcode reader.
    _barcodeReader = await DynamsoftBarcodeReader.createInstance();

    /// Receive the barcode decoding results and store the result in object decodeResults
    _barcodeReader.addResultlistener().listen((List<BarcodeResult> res) {
      if (mounted) {
        setState(() {
          this.decodeResults = res;
        });
      }
    });

    /// Start barcode decoding when the widget is created.
    _barcodeReader.startScanning();

    /// When overlayVisible is set to true, the decoded barcodes will be highlighted with overlays.
    _cameraView.isOverlayVisible = true;
  }
}
```

Add configurations to parse and display the barcode decoding results.

```dart
class _MyHomePageState extends State<MyHomePage> {
  ...
  /// Get listItem
  Widget listItem(BuildContext context, int index) {
    BarcodeResult res = this.decodeResults[index];

    return ListTileTheme(
        textColor: Colors.white,
        // tileColor: Colors.green,
        child: ListTile(
          title: Text(res.barcodeFormatString),
          subtitle: Text(res.barcodeText),
        ));
  }
}
```

### Build the Widget

Modify the **build** method to display the decode barcode results on the widget.

```dart
class _MyHomePageState extends State<MyHomePage> {
  ...
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('HelloWorld'),
      ),
      body: Stack(
        children: [
          Container(
            child: _cameraView,
          ),
          Container(
            height: 200,
            child: ListView.builder(
              itemBuilder: this.listItem,
              itemCount: this.decodeResults.length,
            ),
          ),
        ],
      ));
  }
}
```

### Configure Camera Permissions

Before you run the project on iOS devices, you have to add the camera permission first. You can use the following steps to add the camera permission.

1. In the **ios** folder of your project, find **Runner.xcworkspace**. Open it.
2. In the **info.plist** of the project, add **Privacy - Camera Usage Description**.

### Run the Project

In terminal, go to the project folder and run the following command:

```bash
flutter run
```

> Notes:
>
> - When running Android, you might have to add `minSdkVersion 21` in your build.gradle(app) before running the project on Android devices.
> - When running iOS, you might have to open the Xcode and go to the **Deployment Info** section of the project to switch the iOS version to 10.0+.

## Customizing the Barcode Reader

### Using the Settings Templates

DBR offers several preset templates for different popular scenarios. To prioritize speed over accuracy, then you will want to use one of the speed templates, choosing the corresponding template for images or video, respectively. And vice versa if you’re looking to prioritize read rate and accuracy over speed. For the full set of templates, please refer to EnumPresetTemplate. Here is a quick example:

```dart
await _barcodeReader.updateRuntimeSettingsFromTemplate(template: EnumDBRPresetTemplate.VIDEO_READ_RATE_FIRST );
```

### Using the DBRRuntimeSettings Interface

The SDK also supports a more granular control over the individual runtime settings rather than using a preset template. The main settings that you can control via this interface are which barcode formats to read, the expected number of barcodes to be read in a single image or frame, and the timeout. For more info on each, please refer to DBRRuntimeSettings. Here is a quick example:

```dart
DBRRuntimeSettings currentSettings = await _barcodeReader.getRuntimeSettings();
currentSettings.barcodeFormatIds = EnumBarcodeFormat.BF_ONED;
currentSettings.expectedBarcodeCount = 10;
currentSettings.timeout = 500;
try {
  await _barcodeReader.updateRuntimeSettings(settings: currentSettings);
} catch (e) {
  print('error = $e');
}
```

### Customizing the Scan Region

You can also limit the scan region of the SDK so that it doesn’t exhaust resources trying to read from the entire image or frame. In order to do this, we will need to use the Region interface as well as the DynamsoftCameraView component.

First, the region must be defined using the Region interface. In this example, we demonstrate how the region is first defined in the render() function and then assigned to the scanRegion parameter of the DynamsoftCameraView component:

```dart
final DynamsoftCameraView _cameraView = DynamsoftCameraView();
Region scanRegion = Region(regionTop: 20, regionBottom: 80, regionLeft: 20, regionRight: 80, regionMeasuredByPercentage: true);
_cameraView.scanRegion = scanRegion;
```

## Get a License Key

- The `BarcodeReader` module of Dynamsoft Capture Vision needs a valid license to work.
- A time-limited public trial license is available for every new device for the first use of Dynamsoft Capture Vision.
- If your public trial key is expired, please visit <a href="https://www.dynamsoft.com/customer/license/trialLicense?product=dbr&utm_source=docs" target="_blank">Private Trial License Page</a> to get a 30-day trial extension.
- [Contact Us](https://www.dynamsoft.com/company/contact/)  to purchase a full license.
