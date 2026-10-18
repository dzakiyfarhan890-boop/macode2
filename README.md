# Al-Qur’an Offline (Android)

Pembungkus WebView untuk `alquran-offline.html`. Seluruh data ada di dalam aplikasi, tanpa internet dan tanpa izin INTERNET.

## Build lewat GitHub
1. Buat repositori baru di GitHub, lalu unggah seluruh isi folder ini (termasuk folder `.github`).
2. Buka tab **Actions**. Workflow *Build APK* berjalan otomatis setiap push (atau jalankan manual lewat *Run workflow*).
3. Setelah selesai, buka run tersebut, lalu unduh artifact **alquran-offline-debug-apk** (isinya `app-debug.apk`).
4. Salin APK ke ponsel dan pasang (izinkan "pasang dari sumber tidak dikenal").

## Memperbarui isi aplikasi
Ganti `app/src/main/assets/index.html` dengan versi terbaru, lalu push. Naikkan `versionCode` di `app/build.gradle` bila ingin memasang di atas versi lama.

## Mengganti nama, ID, ikon
- Nama aplikasi: `app/src/main/res/values/strings.xml`
- ID aplikasi: `applicationId` dan `namespace` di `app/build.gradle` (bila namespace diubah, ubah juga nama paket pada `MainActivity.java`)
- Ikon: ganti `res/drawable/ic_launcher.xml`, atau buat ikon lengkap lewat Android Studio (Image Asset)

## Untuk Google Play
APK debug hanya cocok untuk dipasang sendiri. Untuk Play Store dibutuhkan build release bertanda tangan (AAB) dan `targetSdk` yang memenuhi syarat Play saat itu.
