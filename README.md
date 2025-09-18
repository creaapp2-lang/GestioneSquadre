# Gestione Squadre – APK via GitHub Actions (Capacitor)

Questa repo impacchetta l'app HTML in un'APK Android usando [Capacitor](https://capacitorjs.com/) e GitHub Actions.

## Prerequisiti
- GitHub account
- Node 18+ sulla tua macchina
- (Opzionale) Android Studio se vuoi buildare localmente

## Avvio rapido

```bash
npm install
npm run build
npx cap add android
npx cap sync android
cd android && ./gradlew assembleDebug
# APK: android/app/build/outputs/apk/debug/app-debug.apk
```

## Build automatica su GitHub
1. Crea una nuova repo su GitHub e fai push di questi file su `main`.
2. Vai su **Actions** → vedrai il workflow **Build Android APK** partire ad ogni push.
3. Al termine, scarica l'artifact **app-debug.apk** dal job.

## Firma release (opzionale)
Vedi guida nel workflow e nei commenti. Se vuoi, posso aggiungere io lo step di firma.
