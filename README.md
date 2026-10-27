# Andro AI — Android wrapper

This repository packages the existing deployed AI assistant website as an Android app using Capacitor.

- Live website: https://andro-ai-81bhtj.v2.appdeploy.ai/
- Android app id: `com.androgrokeui.androai`
- Android app name: `Andro AI`
- Build workflow: https://github.com/androgroke-ui/Andro-AI/actions

## Important behavior

The Android app opens the existing hosted website in a Capacitor WebView. Internet access is required; this is not a native/offline AI model and it does not embed API keys. The website's AI/backend remains hosted by AppDeploy.

## Build an APK

Push to `main` or run the **Build and Verify** workflow manually. When successful, download the `andro-ai-debug-apk` artifact from the completed workflow run. The APK is a debug build intended for testing, not a signed Play Store release.

## Local build

Requires Node.js 20, Java 17, and the Android SDK.

```sh
npm install
npx cap add android
npx cap sync android
cd android
./gradlew assembleDebug
```

APK output: `android/app/build/outputs/apk/debug/app-debug.apk`.
