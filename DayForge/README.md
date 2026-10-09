# DayForge — offline Android app

DayForge is a simple, offline-first personal routine tracker and to-do app for a college minor project.

## Included features
- Home dashboard with daily progress
- Daily habit/counter tracking: water, study time, coding sessions, showers
- Add a simple custom counter with a daily target
- Study session timer
- To-do list with optional date/time reminder
- Local weight log and basic history
- Data stored locally in the app's WebView local storage
- Android notification scheduling bridge for task reminders

## Build APK
1. Install Android Studio on a computer.
2. Extract this ZIP.
3. In Android Studio, choose **Open** and select the extracted `DayForge` folder.
4. Allow Gradle sync to finish. Android Studio may download the Android Gradle Plugin and SDK platform.
5. Connect an Android phone with USB debugging enabled, or use an emulator, and press **Run** to test.
6. To create an APK: **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
7. The debug APK is normally created at `app/build/outputs/apk/debug/app-debug.apk`.

## Notes
- No account or internet connection is needed for app features once installed.
- On Android 13+, allow notifications when prompted to receive reminders.
- Reminder delivery depends on device notification settings and Android power-management behaviour.
- The current version is a simple submission-focused build, not a production-grade health or scheduling product.

## Build APK online (without installing Android Studio on your phone)
This repository includes `.github/workflows/build-apk.yml` for GitHub Actions.
1. Create a GitHub repository and upload the contents of this folder.
2. Open the repository's **Actions** tab and run **Build DayForge APK** (or push to `main`).
3. Wait for the workflow to finish.
4. Open the successful workflow run and download the `DayForge-debug-apk` artifact.
5. Extract the artifact ZIP; it contains `app-debug.apk`.
6. Transfer the APK to an Android phone and install it. Android may ask you to allow installing unknown apps for the app you used to open the file.

This creates a debug APK for testing/submission, not a Play Store release. It targets Android 8.0+ (API 26+) and is not installable on iPhones.
