# TWRP Device Info Collector

An Android application that automatically collects all device information needed for [Hovatek Online TWRP Builder](https://www.hovatek.com/twrpbuilder/).

## Features

- 📱 Automatically collects comprehensive device information
- 💾 Saves data to `sdcard/Download/twrp-builder-{codename}.txt`
- 🔍 Gathers all required information for TWRP Builder:
  - Device codename, brand, model, manufacturer
  - Android version and API level
  - Screen resolution
  - CPU architecture (ABI)
  - Kernel version
  - Build fingerprint
  - Hardware information
  - And much more!

## What is this for?

This app helps you gather all the technical information about your Android device that is required when using the Hovatek Online TWRP Builder to create a custom TWRP recovery for your device.

## How to Use

1. Install the APK on your Android device
2. Open the "TWRP Info Collector" app
3. The app will automatically collect your device information
4. Tap "Save to File" to save the information
5. Find the file at: `sdcard/Download/twrp-builder-{your-device-codename}.txt`
6. Use this information when building TWRP at https://www.hovatek.com/twrpbuilder/

## Building the APK

### Prerequisites

- Android SDK (API level 33 or higher)
- Java Development Kit (JDK) 8 or higher
- Gradle 7.4.2 or higher

### Build Instructions

#### Option 1: Using Gradle (Command Line)

```bash
# Clone the repository
git clone https://github.com/kay6888/Hovatek--Online--TWRP--Builder-help.git
cd Hovatek--Online--TWRP--Builder-help

# Build the debug APK
./gradlew assembleDebug

# Or build the release APK (unsigned)
./gradlew assembleRelease

# The APK will be located at:
# app/build/outputs/apk/debug/app-debug.apk
# or
# app/build/outputs/apk/release/app-release-unsigned.apk
```

#### Option 2: Using Android Studio

1. Open Android Studio
2. Click "Open an Existing Project"
3. Navigate to and select the cloned repository folder
4. Wait for Gradle to sync
5. Click "Build" → "Build Bundle(s) / APK(s)" → "Build APK(s)"
6. The APK will be in `app/build/outputs/apk/`

### Installing the APK

1. Transfer the APK to your Android device
2. Enable "Install from Unknown Sources" in your device settings
3. Open the APK file and install it

## Information Collected

The app collects the following information:

- **Basic Device Info**: Codename, Product Name, Brand, Model, Manufacturer, Board, Hardware
- **Android Version Info**: Android Version, API Level, Build ID, Build Type, Tags
- **Architecture Info**: Supported ABIs, Primary ABI, CPU Architecture
- **Screen Info**: Resolution, Density, Density Scale
- **Kernel Info**: Kernel Version, Detailed Kernel Information
- **Build Info**: Fingerprint, Display, Bootloader, Radio Version
- **Additional Properties**: Host, User, Build Time

## Permissions

The app requires storage permissions to save the device information file:

- `WRITE_EXTERNAL_STORAGE` (Android 9 and below)
- Scoped storage access (Android 10+)

## Compatibility

- Minimum Android Version: 5.0 (Lollipop, API 21)
- Target Android Version: 13 (API 33)
- Supports all Android architectures (ARM, ARM64, x86, x86_64)

## Output File Format

The app saves all information in a plain text file with clear sections:

```
=== TWRP BUILDER DEVICE INFORMATION ===

--- BASIC DEVICE INFO ---
Device Codename: [your device codename]
Brand: [your device brand]
Model: [your device model]
...

=== TWRP BUILDER REQUIREMENTS ===
Android Version: [version]
Screen Resolution: [width]x[height]
Device Codename: [codename]
...

=== INSTRUCTIONS ===
[Step-by-step guide for using Hovatek TWRP Builder]
```

## About TWRP Builder

TWRP (Team Win Recovery Project) is a custom recovery image for Android devices. The Hovatek Online TWRP Builder is a service that helps you build a custom TWRP recovery for your specific device model.

Visit: https://www.hovatek.com/twrpbuilder/

## License

This project is open source and available for anyone to use and modify.

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests.

## Support

For issues with the app, please open an issue on GitHub.
For TWRP Builder support, visit: https://www.hovatek.com/forum/

## Disclaimer

This app only collects and displays device information. It does not root your device, modify system files, or make any changes to your device. Use the collected information at your own risk when building custom recovery images.
