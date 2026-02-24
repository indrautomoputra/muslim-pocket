
# 🕌 Muslim Pocket - Aplikasi Ibadah Digital Sederhana (v2.5)

[![GitHub license](https://img.shields.io/github/license/indrautomoputra/Muslim-Pocket?style=flat-square)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/indrautomoputra/Muslim-Pocket?style=flat-square)](https://github.com/indrautomoputra/Muslim-Pocket/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/indrautomoputra/Muslim-Pocket?style=flat-square)](https://github.com/indrautomoputra/Muslim-Pocket/network/members)
[![App Version](https://img.shields.io/badge/version-2.5-blue.svg?style=flat-square)](CHANGELOG.md)

Muslim Pocket adalah aplikasi web sederhana yang dirancang untuk membantu umat Muslim dalam menjalankan ibadah sehari-hari. Aplikasi ini dibangun menggunakan Google Apps Script dan menyajikan fitur-fitur penting seperti tasbih digital, kumpulan doa & dzikir, jadwal imsakiyah, dan arah kiblat.

## ✨ Fitur Utama

-   **📿 Tasbih Digital:**
    -   Penghitung tasbih yang mudah digunakan.
    -   Pengaturan target hitungan (11, 33, 99, atau kustom).
    -   Fitur mute untuk pengalaman yang lebih fokus.
    -   Penyimpanan hitungan dan target secara otomatis (menggunakan Google Apps Script PropertiesService).
-   **📚 Doa & Dzikir Pilihan:**
    -   Kumpulan doa dan dzikir penting (Ayat 1000 Dinar, Ayat Kursi, Akhir Al-Kahfi, Doa Makan, Doa Tidur, Dzikir Pagi).
    -   **Tambahan:** Doa-doa para Nabi dan Rasul (Nabi Adam, Nabi Yunus, Nabi Musa, Nabi Ibrahim, Doa Perlindungan Nabi Muhammad SAW).
    -   Lengkap dengan teks Arab, transliterasi Latin, dan terjemahan Bahasa Indonesia.
    -   Fitur menyalin teks doa/dzikir ke clipboard.
-   **🗓️ Jadwal Imsakiyah & Salat:**
    -   Menampilkan jadwal salat dan imsakiyah bulanan untuk wilayah Makassar, Sulawesi Selatan.
    -   Secara otomatis menyoroti hari ini dan waktu salat yang sedang berlangsung (atau yang berikutnya).
    -   Data diambil dari API eksternal (aladhan.com).
-   **🧭 Arah Kiblat:**
    -   Menghitung dan menampilkan arah Kiblat (derajat dari Utara Sejati) berdasarkan lokasi geografis pengguna saat ini.
-   **🎨 Mode Gelap / Terang:**
    -   Pilihan tampilan mode gelap atau terang sesuai preferensi pengguna.
    -   Pengaturan mode disimpan di browser (localStorage).
-   **📱 Desain Responsif:**
    -   Aplikasi dapat diakses dengan nyaman di berbagai perangkat, dari ponsel hingga desktop.
-   **🔒 Privasi:**
    -   Tidak ada iklan, tidak ada analitik, data pribadi aman dan tidak dikumpulkan.

## 🛠️ Teknologi yang Digunakan

-   **Google Apps Script (GAS):** Sebagai backend dan hosting aplikasi web.
-   **HTML5:** Struktur dasar halaman.
-   **CSS3:** Styling dan tema (mode gelap/terang).
-   **JavaScript (Vanilla JS):** Logika frontend dan interaksi pengguna.
-   **Geolocation API:** Untuk fitur arah kiblat.
-   **Aladhan.com API:** Untuk data jadwal salat.

## 🚀 Instalasi & Deployment

Aplikasi ini dirancang untuk di-deploy sebagai Aplikasi Web Google Apps Script.

### Langkah-langkah Deployment:

1.  **Buat Proyek Apps Script Baru:**
    *   Buka [script.google.com/home](https://script.google.com/home).
    *   Klik `New project` atau `Proyek baru`.
2.  **Siapkan File Code.gs:**
    *   Secara default, akan ada file `Code.gs`. Ubah isinya dengan code yang ada di `Code.gs` dari proyek ini (jika ada, atau buat manual jika kosong). File ini biasanya berisi fungsi `doGet()` untuk melayani aplikasi web.
3.  **Buat File index.html:**
    *   Di editor Apps Script, klik `File` > `New` > `HTML file`. Beri nama `index.html`.
    *   Salin seluruh konten dari `index.html` dari proyek ini dan tempelkan ke file `index.html` yang baru Anda buat di Apps Script.
4.  **Simpan Proyek:**
    *   Klik ikon disket (Save project) atau `Ctrl + S`. Beri nama proyek Anda, contoh: `Muslim Pocket`.
5.  **Deploy sebagai Aplikasi Web:**
    *   Klik `Deploy` (panah ke bawah di kanan atas), lalu pilih `New deployment`.
    *   Pilih jenis deployment: `Web app`.
    *   Konfigurasi deployment:
        -   **Description:** (Opsional) Beri deskripsi singkat seperti "Initial Deployment" atau "v2.5 Features".
        -   **Execute as:** `Me (your_email@gmail.com)`
        -   **Who has access:** `Anyone` (atau `Anyone, even anonymous` jika Anda ingin aplikasi dapat diakses tanpa login Google).
    *   Klik `Deploy`.
    *   Jika ini deployment pertama, Anda mungkin akan diminta untuk memberikan otorisasi kepada Apps Script untuk mengakses layanan Google tertentu (misalnya `PropertiesService` untuk menyimpan data tasbih). Ikuti petunjuk untuk mengotorisasi.
    *   Setelah berhasil, Anda akan mendapatkan `Web app URL`. Salin URL ini.
6.  **Akses Aplikasi:**
    *   Buka browser Anda dan tempelkan `Web app URL` yang telah Anda salin.
    *   **Penting:** Saat memperbarui aplikasi (setelah ada perubahan kode), selalu lakukan `Deploy` > `Manage deployments` > `Edit deployment` (ikon pensil) > pilih **`New version`** di bagian `Version` > `Deploy`. Setelah itu, lakukan **Hard Refresh** pada halaman aplikasi di browser (`Ctrl + Shift + R` atau `Cmd + Shift + R`) untuk memastikan semua perubahan dimuat.

## 📄 Struktur Proyek

```
.
├── Code.gs             # Backend logic using Google Apps Script
├── index.html          # Frontend HTML, CSS, and JavaScript for the web app
└── README.md           # This file
```

## 🌐 Sumber Data Eksternal

-   **API Jadwal Salat:** [aladhan.com](https://aladhan.com/prayer-times-api)

## 🤝 Kontribusi

Kami menyambut kontribusi! Jika Anda memiliki ide untuk fitur baru, perbaikan bug, atau peningkatan lainnya, silakan:

1.  Fork repositori ini.
2.  Buat branch fitur baru (`git checkout -b feature/AmazingFeature`).
3.  Lakukan perubahan Anda.
4.  Commit perubahan Anda (`git commit -m 'Add some AmazingFeature'`).
5.  Push ke branch (`git push origin feature/AmazingFeature`).
6.  Buka Pull Request.

## 📝 Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE).

## 🧑‍💻 Tentang Pengembang

Dibuat dengan semangat untuk memudahkan ibadah Anda oleh indrautomoputra.
