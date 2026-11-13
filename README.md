# The Simran — Android app project

This Android Studio project wraps the supplied birthday-wishes and romantic-songs HTML page in a native Android WebView app. The original HTML (including its embedded image and JavaScript) is included at `app/src/main/assets/index.html`.

## Build an installable APK with GitHub Actions (no Android SDK needed on your PC)

1. Extract this ZIP.
2. Create a new GitHub repository and upload the **contents** of this folder (so `app/`, `build.gradle`, `settings.gradle`, and `.github/` are at the repository root).
3. Open the repository's **Actions** tab. Select **Build The Simran APK** and click **Run workflow** (or let the first push trigger it).
4. When the run finishes successfully, open that run and download the **The-Simran-Android-APK** artifact.
5. Extract the artifact on your phone and tap `app-debug.apk` to install. If Android asks, allow your browser/file manager to install unknown apps.

## Build locally with Android Studio

Open this folder in Android Studio, allow Gradle sync, then choose **Build → Build Bundle(s) / APK(s) → Build APK(s)**. The debug APK will be at `app/build/outputs/apk/debug/app-debug.apk`.

## Notes

- The app opens the supplied page locally; the HTML and embedded image are packaged inside the APK.
- The page currently loads Tailwind CSS and Google Fonts from their online CDNs and opens YouTube/search links externally, so those parts need an internet connection. The app itself does not contain licensed full-length music files; the page's built-in “Play Chime” is a generated tone preview.
- This is a debug APK build setup, suitable for personal installation and testing. A Play Store release would need a separately signed release build.
