# 🕌 Masjid Raya Darussalam - Website Wisata Religi

Website profil dan wisata religi Masjid Raya Darussalam Samarinda, Kalimantan Timur. Dibangun sebagai Projek Akhir mata kuliah Pemrograman Aplikasi Bergerak.

---

## Tim Pengembang

**Kelompok 7 Hara Hetta** — Sistem Informasi C 2024  
Mata Kuliah: Pemrograman Aplikasi Bergerak

| No | Nama | NIM | GitHub |
|----|------|-----|--------|
| 1 | Yulius Pune' | 2409116110 | [@Oxcyy](https://github.com/Oxcyy) |
| 2 | Muhammad Fakhri Al-Kautsar | 2409116081 | [@kksgaa](https://github.com/kksgaa) |
| 3 | Yudha Tri Atmaja | 2409116095 | [@Yudhatriatmajaa](https://github.com/Yudhatriatmajaa) |
| 4 | Elvira Agustin | 2409116109 | [@elviraags](https://github.com/elviraags) |
| 5 | Rizky Wahyu Dina Putri | 2409116111 | [@Dinaapp](https://github.com/Dinaapp) |

---

## Deskripsi Aplikasi

**Masjid Raya Darussalam** adalah website resmi yang menampilkan informasi lengkap tentang Masjid Raya Darussalam Samarinda sebagai destinasi wisata religi di Kalimantan Timur. Website ini menyediakan informasi fasilitas, galeri foto, video kegiatan, jadwal sholat real-time, serta sistem ulasan jamaah yang interaktif.

Website dibangun menggunakan **PHP native**, **MySQL** sebagai database, **Bootstrap 5** untuk tampilan responsif, dan **Vue.js 3** untuk komponen interaktif seperti jadwal sholat dan form ulasan.

---

## Fitur Website

### Halaman Publik
- **Beranda** — Hero section dinamis, statistik, galeri foto, video YouTube, dan ulasan terbaru
- **Jadwal Sholat** — Tampil real-time via API aladhan.com menggunakan Vue.js 3, lengkap dengan countdown waktu sholat berikutnya dan fallback data lokal Samarinda
- **Detail & Fasilitas** — Profil lengkap masjid beserta daftar fasilitas dengan foto
- **Galeri Foto** — Tampilan grid interaktif dengan lightbox
- **Ulasan Jamaah** — Form kirim ulasan dengan rating bintang (1-5) dan filter ulasan reaktif
- **Responsive Design** — Tampil optimal di semua ukuran layar

### Panel Admin
- **Dashboard** — Statistik lengkap: total ulasan, rating, fasilitas, foto, dan video
- **Moderasi Ulasan** — Approve, edit, dan hapus ulasan masuk
- **Kelola Fasilitas** — CRUD data fasilitas lengkap dengan foto
- **Kelola Galeri & Video** — Manajemen foto galeri dan embed YouTube dalam satu halaman
- **Floating Admin Bar** — Akses cepat ke dashboard saat melihat tampilan publik

### Keamanan
- Password admin dicek menggunakan `password_hash()` (bcrypt)
- Semua query database menggunakan PDO Prepared Statement, aman dari SQL Injection
- CSRF Token Protection pada setiap form admin
- Validasi MIME type nyata untuk upload foto (bukan hanya ekstensi)
- Session auto-expire 1 jam + regenerate ID saat login
- Folder uploads dilindungi `.htaccess` agar tidak bisa diakses langsung

---

## Teknologi yang Digunakan

| Kategori | Teknologi |
|----------|-----------|
| Backend | PHP 8.0+, PDO MySQL |
| Frontend | Bootstrap 5.3, Font Awesome 6.5 |
| JavaScript | Vue.js 3 (CDN), Vanilla JS (Fetch API) |
| Database | MySQL / MariaDB |
| Server | Apache + mod_rewrite (Laragon) |
| API Eksternal | aladhan.com (jadwal sholat) |

---

## Struktur Folder

```
masjid/
├── index.php                   # Halaman Beranda
├── .htaccess                   # Routing & keamanan Apache
├── api/                        # REST API endpoint (JSON)
│   ├── auth.php                # Login & logout admin
│   ├── reviews.php             # CRUD ulasan
│   ├── facilities.php          # CRUD fasilitas
│   ├── gallery.php             # CRUD galeri foto
│   └── video.php               # CRUD video YouTube
├── assets/
│   ├── css/style.css           # Stylesheet utama
│   └── js/
│       ├── controller.js       # Logic frontend
│       ├── vue-prayer.js       # Komponen Vue jadwal sholat
│       └── vue-reviews.js      # Komponen Vue form & list ulasan
├── includes/
│   └── config.php              # Konfigurasi DB, session, helper
├── views/
│   ├── detail.php              # Halaman detail & fasilitas
│   ├── ulasan.php              # Halaman ulasan
│   ├── login.php               # Halaman login admin
│   └── admin/
│       ├── dashboard.php
│       ├── kelola_fasilitas.php
│       ├── kelola_galeri.php
│       ├── kelola_ulasan.php
│       ├── kelola_video.php
│       ├── _sidebar.php
│       └── _footer.php
└── uploads/                    # File foto yang diupload
    ├── facilities/
    ├── gallery/
    └── reviews/
```

---

## Cara Menjalankan

**1. Clone repositori**
```bash
git clone https://github.com/Oxcyy/Masjid-Raya-Darussalam.git
```

**2. Pindahkan ke folder server**
```
Salin folder ke: C:/laragon/www/
```

**3. Buat database**
```sql
CREATE DATABASE masjidraya CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

**4. Konfigurasi koneksi** — edit `includes/config.php`
```php
define('DB_HOST', 'localhost');
define('DB_NAME', 'masjidraya');
define('DB_USER', 'root');
define('DB_PASS', '');
```

**5. Akses aplikasi**
```
http://localhost/masjid/                  -> Halaman Publik
http://localhost/masjid/views/login.php   -> Login Admin
```
