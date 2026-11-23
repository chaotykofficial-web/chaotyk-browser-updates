# Chaotyk Arcade — Android 1.1.3

Standalone offline Android app containing the Chaotyk Arcade 3.12.0 collection: all 18 games, including Chain Panic and Layup Launch. Requires Android 8.0 or later and an up-to-date Android System WebView. No browser extension, website login, or network connection is needed to play.

## Install

Download Chaotyk-Arcade-1.1.3.apk to the Android device, open it, and allow installation from the downloading app if Android asks. Open Chaotyk Arcade. Keep Chaotyk Browser installed if desired: these are separate applications.

The ⋮ button opens App updates and About. Android Back returns to the Arcade menu, then asks before exiting. Backgrounding the app or opening a native dialog pauses play; tap Resume playing when returning. Scores and settings persist locally. Leaderboard export/import uses Android's document picker. Uninstalling or clearing app data removes local scores/settings.

Updates check after opening/resuming and every five minutes while the app is visible. Updates require internet access and user approval to install. Android may ask to allow updates from Chaotyk Arcade. Future updates must retain package com.chaotyk.arcade and the same signing certificate. The updater checks package, advertised version, increasing Android versionCode, and signer before installation.

## Build

Use JDK 17 or newer and Android SDK platform 35 / build-tools 35.0.0. Set ANDROID_SDK_ROOT. Supply the private signing key at signing/chaotyk-arcade.jks and its password in environment variable ARCADE_KEYSTORE_PASSWORD, then run bash build.sh. The private signing key is intentionally excluded from public source downloads. Keep the private project backup to produce compatible future updates.

For a release, update MainActivity.VERSION, build.sh version name/code, shell subtitle, and the release feed. Build, verify, test, then publish the new versioned APK and update app-update.txt. Do not change the Browser release feed at repository root.

## Validation

APK compiled and verified with Android build tools. Browser tests cover all 18 launches, touch control buttons, flag mode, menus/cleanup, Chaotyk setup, saved data, escaped imported labels, export handoff, pause/resume overlay, portrait/landscape, and offline resource loading. Native updater tests cover version/package/certificate checks, redirects, invalid files, truncation, and cancellation. A physical Android install, document pickers, sound, background behavior, and an actual update-install cycle still require device testing.

## 1.1.3
GigaGems now uses six distinct colorful icons: diamond, flame, clover, star, cherries and grapes. Larger shaded pieces and separate power markers improve phone readability. Game rules unchanged.
GigaGems tested in both modes on a phone-size board, including swaps, scoring, power markers, Shuffle, Detonate and restart.
