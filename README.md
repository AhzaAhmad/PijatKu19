# PijatKu - Aplikasi Android (WebView)

Aplikasi booking pijat berbasis WebView. Semua UI ada di `app/src/main/assets/index.html`.

## Fitur
- WebView dengan JavaScript & DOM Storage (localStorage) aktif
- Progress bar saat loading
- Buka tautan WhatsApp (`wa.me`, `whatsapp://`) ke aplikasi WhatsApp
- Dukungan `tel:`, `mailto:`, `sms:`
- Tombol back navigasi WebView

## Cara Build APK di Android Studio

1. Buka **Android Studio**.
2. **File → Open** → pilih folder `pijatku-android-project`.
3. Tunggu **Gradle Sync** selesai (pertama kali bisa lama karena download dependency).
4. Menu **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. Setelah selesai, klik **locate** pada notifikasi.
6. File APK ada di:
   ```
   app/build/outputs/apk/debug/app-debug.apk
   ```

## Cara Instal di HP
1. Pindahkan `app-debug.apk` ke HP Android.
2. Buka file tersebut.
3. Izinkan **Install unknown apps** jika diminta, lalu ketuk **Install**.

## Build Signed APK (untuk rilis)
1. **Build → Generate Signed Bundle / APK**.
2. Pilih **APK** → Create new keystore (atau gunakan yang sudah ada).
3. Isi data keystore, lalu pilih **release**.
4. File hasil: `app/release/app-release.apk`

## Struktur Proyek
```
pijatku-android-project/
├── app/
│   ├── build.gradle.kts
│   ├── proguard-rules.pro
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── assets/index.html          ← UI utama aplikasi
│       ├── java/.../MainActivity.kt
│       └── res/
├── build.gradle.kts
├── settings.gradle.kts
└── README.md
```

## Catatan
- `minSdk = 24` (Android 7.0+)
- `targetSdk = 34`
- Icon launcher sudah disediakan (warna hijau tema PijatKu)
- Tema Material 3 DayNight tanpa ActionBar
