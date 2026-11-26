# FitTrack Android app

A WebView wrapper around the FitTrack web app (app/src/main/assets/index.html).

## Build the APK (Android Studio, about 5 minutes)

1. Install Android Studio (https://developer.android.com/studio). It includes the Android SDK and JDK 17.
2. Unzip this folder. In Android Studio choose File > Open and select the FitTrackApk folder.
3. Wait for the Gradle sync. Android Studio creates the Gradle wrapper automatically.
4. Build the APK: Build > Build Bundle(s) / APK(s) > Build APK(s).
5. Click "locate" in the notification. The file is at app/build/outputs/apk/debug/app-debug.apk.
6. Copy it to your phone and install it. Allow "Install unknown apps" for your file manager when prompted.

For a signed release APK: Build > Generate Signed App Bundle / APK, create a keystore, and choose APK.

## Notes

- Internet permission is needed for the Chart.js charts (loaded from cdnjs). Charts will not render offline.
- GPS works when location permission is granted. If denied, the app estimates distance instead.
- Data is stored in the WebView's local storage on the device. Uninstalling the app deletes it.
- To update the app, replace app/src/main/assets/index.html with a newer version and rebuild.
- Before publishing to Google Play, change applicationId in app/build.gradle.kts to your own reverse-domain ID, and replace the default icon with your own.
