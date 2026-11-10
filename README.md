# Data Entry Excel (Android)

Aplikasi Android offline untuk entry data dengan kriteria dinamis dan ekspor XLSX.

## Fitur
- Dua halaman: ENTRY dan DATA.
- Ubah nama kriteria langsung pada kolom kiri.
- Tambah dan hapus kriteria.
- SAVE menyimpan satu record lalu mengosongkan input.
- Data disimpan lokal memakai SQLite.
- Cari, edit, dan hapus record.
- Ekspor `.xlsx` melalui pemilih lokasi Android; hasil dapat dibuka di WPS Office.
- Tidak membutuhkan koneksi internet saat aplikasi digunakan.

## Build
Proyek memakai Android Gradle Plugin 8.7.3, Gradle 8.9, JDK 17, compileSdk 35, minSdk 23.

1. Ekstrak ZIP.
2. Buka folder `DataEntryExcel` sebagai proyek Gradle di IDE Android yang mendukung AGP 8.7.3.
3. Tunggu Gradle sync selesai.
4. Pilih Build APK / Assemble Debug.
5. APK debug biasanya berada di `app/build/outputs/apk/debug/app-debug.apk`.

Catatan: proyek sumber ini belum dikompilasi atau diuji pada perangkat fisik. Untuk build pertama, IDE perlu mengunduh Gradle dan Android SDK/build tools.

## Build APK online tanpa memasang IDE di HP

ZIP ini menyertakan GitHub Actions workflow.

1. Buat repository baru di GitHub melalui browser dan pilih repository kosong.
2. Ekstrak ZIP ini, lalu unggah seluruh isi folder proyek (termasuk folder tersembunyi `.github`) ke repository. Pastikan `settings.gradle` berada di tingkat paling atas repository.
3. Buka tab Actions pada repository. Jika diminta, aktifkan Actions.
4. Pilih workflow `Build Android APK`, lalu tekan `Run workflow`.
5. Setelah proses selesai (status hijau), buka hasil run dan unduh artifact `DataEntryExcel-debug-apk`.
6. Ekstrak artifact ZIP; di dalamnya ada `app-debug.apk`. Pasang APK di Android.

Build online membutuhkan internet dan akun GitHub. Setelah APK terpasang, aplikasi berjalan offline.
