# Cara Build APK tanpa Android Studio (pakai GitHub Actions – GRATIS)

## Langkah-langkah

### 1. Buat akun GitHub (gratis)
Buka: https://github.com/signup

### 2. Buat repository baru
1. Klik tombol **New** (atau + → New repository)
2. Isi **Repository name**: `PijatKu` (boleh diganti)
3. Biarkan **Public**
4. Jangan centang "Add a README"
5. Klik **Create repository**

### 3. Upload folder proyek
Ada 2 cara:

**Cara A – Paling mudah (lewat browser)**
1. Di halaman repository yang baru dibuat, klik **uploading an existing file**
2. Drag & drop **semua isi** folder `pijatku-android-project`  
   (bukan foldernya, tapi isinya: `app`, `build.gradle.kts`, `.github`, dll)
3. Tulis commit message: `Initial commit`
4. Klik **Commit changes**

**Cara B – Pakai GitHub Desktop / git** (opsional)

### 4. Jalankan build
1. Di repository GitHub, klik tab **Actions**
2. Klik workflow **Build APK** di sebelah kiri
3. Klik tombol **Run workflow** → **Run workflow**
4. Tunggu 3–7 menit sampai muncul tanda hijau ✓

### 5. Download APK
1. Setelah selesai (hijau), klik pada run yang baru saja
2. Scroll ke bawah ke bagian **Artifacts**
3. Klik **PijatKu-APK**
4. File `app-debug.apk` akan terdownload
5. Pindahkan ke HP Android dan install

---

## Catatan
- Build pertama biasanya lebih lama karena download dependency.
- Artifact (APK) hanya tersimpan 14 hari di GitHub.
- Kalau ada error, buka log di tab Actions dan kirimkan pesannya.

## Alternatif lain
| Cara | Keterangan |
|------|------------|
| Pinjam komputer teman / warnet | Install Android Studio sekali, build, lalu ambil APK |
| Jasa build online berbayar | Codemagic, Bitrise, Appcircle (ada free tier terbatas) |
| Minta tolong orang yang punya Android Studio | Kirimkan ZIP proyek ini |
