# Android Debug APK

This project is prepared for GitHub Actions Android Debug APK builds.

Workflow:
1. `npm install`
2. `npm run build`
3. `npx cap add android`
4. `npx cap sync android`
5. `./gradlew assembleDebug`
6. APK is uploaded as the `zarbyar-debug-apk` artifact.

The generated APK path is:
`android/app/build/outputs/apk/debug/app-debug.apk`

The workflow intentionally uses `npm install` rather than `npm ci`, so a missing
`package-lock.json` does not stop the build.
