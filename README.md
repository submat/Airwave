# AIRWAVE — English Radio Test App

A native Android/Kotlin + Jetpack Compose internet radio prototype using AndroidX Media3 ExoPlayer.

## Included stations
- SomaFM: Groove Salad, Drone Zone, Indie Pop Rocks!, Lush, Underground 80s, Left Coast 70s, Folk Forward

All stations are free to listen to. Streams are delivered by SomaFM; this app does not host or redistribute audio. Stream URLs use SomaFM's published direct-stream hostnames (see https://somafm.com/listen/ and https://somafm.com/listen/uktunein.html). Availability can vary by network and region.

## Build an APK without Android Studio (GitHub Actions)

1. Sign in to GitHub and create a **new repository** (public or private).
2. On the repository page, choose **Add file → Upload files**.
3. Extract this ZIP on your phone or computer, then upload the *contents* of the `EnglishRadioTest` folder. Make sure `.github/workflows/build-apk.yml` is included. On mobile, GitHub's website may be easier to use in desktop mode.
4. Commit the uploaded files to the `main` branch.
5. Open the repository's **Actions** tab. Select **Build AIRWAVE APK** in the left panel, then tap **Run workflow → Run workflow** if it has not already started after the commit.
6. Open the completed run. Under **Artifacts**, download **AIRWAVE-debug-APK**.
7. Extract the downloaded artifact ZIP. It contains `app-debug.apk`. Open that APK on your Android phone and approve installation from that source if Android asks.

The workflow provisions Java 17, Android SDK 35 and Gradle 8.9 in GitHub's cloud runner. No signing key or GitHub secret is required for this debug APK. The artifact is retained for 14 days.

## Local build (optional)
Open this folder in Android Studio, allow Gradle sync, then use **Build → Build Bundle(s) / APK(s) → Build APK(s)**.

## Notes
- Minimum Android version: Android 8.0 (API 26).
- Internet permission is required.
- This prototype keeps playback in the activity; playback may pause when the app is backgrounded or closed. Background playback and lock-screen controls can be added in a later release.
- Stream availability is controlled by each broadcaster and may vary by region or change without notice.
