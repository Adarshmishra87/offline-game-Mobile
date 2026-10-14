# Arcade 100 (offline)
All games are plain HTML5 canvas in `www/` — no internet needed. Capacitor wraps it into an APK.

## Get the APK (no Android Studio needed)
1. Create a GitHub repo, push this folder.
2. Actions tab -> "Build APK" -> download `arcade100-apk` -> unzip -> install app-debug.apk.

## Local build
npm install && npx cap add android && npx cap sync android
cd android && ./gradlew assembleDebug   # needs JDK 17 + Android SDK

## Add a game
1. Copy any file in www/games/, change reg('id','Name','emoji', a=>{...})
2. Add <script src="games/yourgame.js"></script> in www/index.html
Engine API (a): ctx, W, H, loop(dt=>), tap(cb), dir(cb), on(el,ev,fn), setScore(n), text(), restart()
