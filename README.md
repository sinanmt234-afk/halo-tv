# Halo TV — lightweight liquid-glass TV launcher

This project is a redesigned version of the Android Studio / GitHub Actions launcher project you supplied. It keeps the native Java app discovery and launching bridge and the original wallpaper.

## Design
- Translucent liquid-glass navigation capsule, **without costly backdrop blur**.
- Glass glow and border on **only the selected app tile**.
- Five app tiles visible at a time; left/right scrolls through installed apps.
- Remote directional keys, OK/Enter, Back, mouse click.
- No JS frameworks, videos, external fonts, or network resources.

## Build an APK using GitHub
1. Extract this ZIP and upload the **contents of `AppleTVLauncher`** to a new GitHub repository. Keep the `.github/workflows/build.yml` file.
2. Open the repository's **Actions** tab and select **Build APK**.
3. Select **Run workflow** (or push a commit to trigger it).
4. After the workflow completes, open the run and download the **app-debug-apk** artifact.
5. Unzip the artifact to get `app-debug.apk`, then transfer and install it on a compatible Android TV device.

This ZIP is source code, **not a compiled APK**. The project builds using Gradle and Android SDK through GitHub Actions.

## Compatibility
- Android / Android TV devices only (minimum Android 5 / API 21), subject to manufacturer restrictions. Non-Android systems such as LG webOS or Samsung Tizen cannot install Android APKs.
- 2 GB RAM is the optimization target, not a guarantee of lag-free operation.
- The original wallpaper is retained at `app/src/main/assets/wallpaper.jpg`.
- To edit the UI, modify `app/src/main/assets/index.html`.
