# Basic Cordova App

HTML/JS Application Built with Cordova

## Prerequisites
Java, Cordova, Gradle

### Java Development Kit 8
In order to build for Android you will need the latest versions of Java Development Kit installed. Download a copy for your specific machine here: http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html.

### Android SDK
To stay most current and avoid build conflicts, it's recommended to use the official Android Studio install to get Android SDKs and tools on your computer: https://developer.android.com/studio/install.html

When Android Studio opens, click the `Settings` menu to open the Android SDK Manager. You will need to install:
- The highest 'Android SDK Build-tools' version listed
- `Android 7.1.1 (API 25)` - only the `SDK Platform` is required
- Under "Extras", the `Android Support Repository`
- Under "Extras", the `Google Repository`

### Chrome Web Inspector
Application Logs from any developer enabled, connected Android device are available natively in Chrome by going to [chrome://inspect](chrome://inspect). Use these to debug on a device locally, and for all preliminary QA.

### Node v8+ and npm v5+
Install all project dependencies quickly and deterministically. `package-lock.json` should always be committed to the repo.

Usage (Install dependencies): `npm install`

Usage (Add dependencies): `npm install -D [package-name]`

### Cordova v7+
This is necessary to do all builds. https://cordova.apache.org

Install: `npm i -g cordova`

### Testing / Debugging on Mobile Devices ( Android or iOS )
Before deploying to a device, we need to build the right files for each platform.

#### Prepare Platforms and Plugins
If your project folder does not have any reference to 'plugins' or 'platforms' you will need to run this command first to generate the proper platforms and download the correct plugins. Once this is run, you generally will never have to run it again.

Usage: `cordova prepare`

#### Build APK (Development Only)
Depending on the device you wish to test you may run one of the corresponding commands below. This step requires an actual device plugged into your machine. Android will attempt to deploy directly to the device, iOS will open Xcode and the generated project to continue manually from there. It will build a production bundle of the React app, then do a platform build for Cordova.

Android Devices: `cordova run android`


### Device Release
Once you have a working release key it's time to build your release apk. Once complete, the Android apk will be found at `platforms/android/build/outputs/apk/android.apk`.
