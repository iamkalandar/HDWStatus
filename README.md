# ClearStory (Android)

Compresses videos and photos on the phone so WhatsApp Status keeps them sharp.
Web app in `www/index.html`, packaged as an Android app with Capacitor.

## Option A: build the APK on GitHub (no Android Studio)
1. Create a new GitHub repository and upload everything in this folder (keep the `.github` folder).
2. Open the repository's **Actions** tab, choose **Build APK**, tap **Run workflow**.
3. When it finishes (about 5 minutes), open the run and download **ClearStory-debug-apk**.
4. Unzip it, copy `app-debug.apk` to your phone, open it, and allow "install unknown apps" when asked.

## Option B: build with Android Studio
Needs Node 20+ and Android Studio.
```
npm install
npx cap add android
npx cap sync android
npx cap open android
```
In Android Studio press Run, or Build > Build APK(s).

## Notes
- Saving uses the Android share sheet: choose WhatsApp, Files or Drive.
- To change the app, edit `www/index.html`, then run `npx cap sync android` and rebuild.
- Debug APKs are for your own phone. A Play Store release needs a signed release build.
