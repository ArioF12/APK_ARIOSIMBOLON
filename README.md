# 📱 Tugas Prototyping Mobile: WebView dengan MIT App Inventor

Repositori ini berisi dokumentasi tugas mata kuliah **Pemrograman Mobile**. Tugas terdiri dari dua bagian: setup version control (GitHub) dan pembuatan prototipe aplikasi dengan **MIT App Inventor**.

## 👤 Identitas

| | |
|---|---|
| **Nama** | Ario simbolon |
| **NIM** | ISI_NIM |
| **Kelas** | ISI_KELAS |

## ✅ Daftar Tugas

- [x] Membuat akun GitHub
- [x] Mengumpulkan username GitHub ke perwakilan kelas/asisten praktikum
- [x] Membuat project baru di [appinventor.mit.edu](https://appinventor.mit.edu)
- [x] Membuat prototipe dengan komponen WebView
- [x] Menambahkan minimal 1 tombol navigasi
- [x] Export ke file APK
- [ ] Demo di kelas minggu depan

## 1️⃣ Setup Version Control

1. Membuat akun di [github.com](https://github.com).
2. Username GitHub dikumpulkan ke perwakilan kelas/asisten praktikum.
3. Username ini digunakan untuk pengumpulan kode sepanjang semester.

## 2️⃣ Prototipe Aplikasi

### Deskripsi

Aplikasi sederhana yang ketika dibuka **langsung memuat halaman website** berikut:

> 🌐 ISI_URL_WEBSITE (contoh: website kampus atau website berita teknologi)

### Fitur

- 🌐 Memuat halaman website secara otomatis saat aplikasi dibuka
- 🏠 Tombol **Home**: kembali ke halaman awal
- 🔄 Tombol **Refresh**: memuat ulang halaman
- ⬅️ Tombol **Back**: kembali ke halaman sebelumnya (opsional)

### Komponen yang Digunakan

| Komponen | Fungsi |
|---|---|
| `WebViewer1` | Menampilkan halaman website |
| `Button_Home` | Kembali ke halaman utama |
| `Button_Refresh` | Memuat ulang halaman |
| `HorizontalArrangement1` | Menata tombol secara sejajar |

> Catatan: di App Inventor, komponen WebView bernama **WebViewer** (palet *User Interface*).

### Pengaturan Properti

| Komponen | Properti | Nilai |
|---|---|---|
| `WebViewer1` | `HomeUrl` | ISI_URL_WEBSITE |
| `WebViewer1` | `FollowLinks` | ✔ (aktif) |

### Logika Blok

```
when Screen1.Initialize
  do  call WebViewer1.GoHome

when Button_Home.Click
  do  call WebViewer1.GoHome

when Button_Refresh.Click
  do  call WebViewer1.GoToUrl
        url ← WebViewer1.CurrentUrl

when Button_Back.Click
  do  call WebViewer1.GoBack
```

## 📸 Tampilan

<!-- Tambahkan screenshot di folder screenshots/ -->
<!-- ![Designer](screenshots/designer.png) -->
<!-- ![Blocks](screenshots/blocks.png) -->
<!-- ![Hasil di HP](screenshots/hasil.png) -->

## 📦 Cara Export APK

1. Buka project di App Inventor.
2. Klik menu **Build**, lalu pilih **Android App (.apk)**.
3. Tunggu proses selesai, lalu unduh file `.apk` atau scan QR code yang muncul.
4. Di HP Android, izinkan **instal dari sumber tidak dikenal**, lalu pasang APK.

File APK: [`/apk/NAMA_APLIKASI.apk`](apk/)

## ▶️ Cara Mencoba

- **Lewat APK**: instal file APK di HP Android.
- **Lewat emulator/companion**: buka project di App Inventor, lalu sambungkan dengan aplikasi **MIT AI2 Companion**.



## 📚 Referensi

- [MIT App Inventor](https://appinventor.mit.edu)
- [Dokumentasi WebViewer](https://ai2.appinventor.mit.edu/reference/components/userinterface.html#WebViewer)
