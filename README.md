# Aeterna: Android app (preview build)

An Android app that wraps the Aeterna UI (welcome, create a presence, live call, plans, about).
It runs fully offline except for the Google Fonts, which fall back to system fonts if there is no internet.

## Get the APK: option A, no installs (GitHub, free, ~5 minutes)
1. Create a free account at github.com and make a **new empty repository**.
2. Click **Add file → Upload files**, drag in everything from this folder (including the hidden `.github` folder), and commit.
3. Open the repository's **Actions** tab → **Build Aeterna APK** → wait for the green tick.
4. Open that run, download **Aeterna-APK** (a zip), unzip it, and you have `app-debug.apk`.
5. Send the APK to your phone, tap it, and allow "Install unknown apps" when asked.

## Get the APK: option B, Android Studio
1. Install Android Studio and choose **Open** on this folder. Let it sync.
2. **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
3. The file is at `app/build/outputs/apk/debug/app-debug.apk`.

## What works now
- All five screens, the animated logo and the red sparks, and Android's back button.
- Camera and microphone recording, and picking videos, photos and audio from the phone.
- The 7-minute free timer, which keeps counting across app restarts and shows the paywall at zero.
- "Reset free minutes" and "Delete a presence" on the About screen.

## What does not exist yet
- The AI that turns a face and voice into a talking video call. The call screen is a labelled preview.
- Accounts, a server, and real payments (the Choose Eternal button shows a notice).
- The face and voice "enough?" checks currently go by how much you added (one video plus photos, about 30 seconds of audio). Real recognition has to be added with the backend.
- Nothing is uploaded anywhere. Everything stays on the phone.
- This is a debug-signed APK for testing. A Play Store release needs your own signing key.
- iOS: the same `app/src/main/assets/www` folder can be reused in a Capacitor or Xcode WebView project.

Powered by The Pandit Brothers.
