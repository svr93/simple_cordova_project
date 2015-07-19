# Simple Cordova project for iOS and Android development

## Installation Tutorial

1. Install Node.JS v0.10; JDK v1.7 (for Android).
2. Install Android SDK (for Android);
   Xcode 6.0+, iOS 8 SDK (for iOS).

P.S. To install apps onto an iOS device, you must also be a member
of Apple's iOS Developer Program, which costs $99 per year.

3. Install Cordova:
https://www.npmjs.com/package/cordova#installing-from-master

### Android:

1. Set JAVA_HOME, ANDROID_HOME, add .../bin dir (JDK) to PATH,
   add .../tools and .../platform-tools dirs to PATH.

2. cordova platform remove android <br/>
   (before: see version in platforms/platforms.json). <br/>
   cordova platform add android (version)
3. cordova prepare -d
4. cordova compile -d

P.S. You should build app only from the Win console because of special commands
in android.bat file.

P.P.S. In case of building problem
('Could not reserve enough space for object heap'), change
-Dorg.gradle.daemon=true to false in the file
platforms/android/cordova/lib/build.js (it's not good solution, but works).

4.1. Emulation: <br/>
4.1.1. Create device in AVD util. <br/>
4.1.2. cordova run android --emulate <br/>

P.S. In case of emulator problems, copy avd dir from
D:\Users\USERNAME\\.android to C:\Users\USERNAME\\.android

4.2. Real device: <br/>
4.2.1. adb devices <br/>
4.2.2. cordova run android --device <br/>

P.S. In case of 'device offline' problem:
http://www.decker.su/2014/08/adb-device-offline-android-44.html
You need install platform-tools, replace it in SDK dir
IMPORTANT! adb that used by cordova located in C:\Windows. Maybe you need
replace adb (with Adb* dlls) in C:\Windows.
