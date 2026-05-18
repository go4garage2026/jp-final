---
description: Build the Jayti Android debug APK and run E2E tests
---

Build the Jayti Android app and optionally run the E2E test suite.

## Build debug APK
```bash
cd android
./gradlew assembleDebug
```
The APK will be at: `android/app/build/outputs/apk/debug/app-debug.apk`

## Install on connected device
```bash
adb install android/app/build/outputs/apk/debug/app-debug.apk
```

## Run E2E tests (requires connected device or emulator)
```bash
cd android
./gradlew connectedAndroidTest
```

## Build release APK (requires keystore)
```bash
cd android
./gradlew assembleRelease
```

After running the build, tell me:
- ✅ Build succeeded / ❌ Failed with errors
- APK size
- Any Kotlin compilation warnings
- Instructions to install on phone if succeeded
