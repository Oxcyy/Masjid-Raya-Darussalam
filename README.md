# 🕌 Masjid Raya Darussalam - Website Wisata Religi

Website profil dan wisata religi Masjid Raya Darussalam Samarinda, Kalimantan Timur. Dibangun sebagai Projek Akhir mata kuliah Pemrograman Berbasis Web.

---

## Tim Pengembang

**Kelompok 7 Hara Hetta** - Sistem Informasi C 2024  
Mata Kuliah: Pemrograman Berbasis Web

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
- **Beranda** - Hero section dinamis, statistik, galeri foto, video YouTube, dan ulasan terbaru
- **Jadwal Sholat** - Tampil real-time via API aladhan.com menggunakan Vue.js 3, lengkap dengan countdown waktu sholat berikutnya dan fallback data lokal Samarinda
- **Detail & Fasilitas** - Profil lengkap masjid beserta daftar fasilitas dengan foto
- **Galeri Foto** - Tampilan grid interaktif dengan lightbox
- **Lokasi** - Menampilkan lokasi dari masjid raya darussalam dengan embed google maps
- **Ulasan Jamaah** - Form kirim ulasan dengan rating bintang (1-5) dan filter ulasan reaktif
- **Responsive Design** - Tampil optimal di semua ukuran layar

### Panel Admin
- **Dashboard** - Statistik lengkap: total ulasan, rating, fasilitas, foto, dan video
- **Kelola Ulasan** - Approve, edit, dan hapus ulasan masuk
- **Kelola Fasilitas** - CRUD data fasilitas lengkap dengan foto
- **Kelola Galeri & Video** - Manajemen foto galeri dan Video YouTube dalam satu halaman
- **Floating Admin Bar** - Akses cepat ke dashboard saat melihat tampilan publik

---

## Teknologi yang Digunakan

| Kategori | Teknologi |
|----------|-----------|
| Backend | PHP 8.0+, PDO MySQL |
| Frontend | Bootstrap 5.3, Font Awesome 6.5 |
| JavaScript | Vue.js 3 (CDN), Vanilla JS (Fetch API) |
| Database | MySQL |
| Server | Apache + mod_rewrite (Laragon) |
| API Eksternal | aladhan.com (jadwal sholat) |

---

## Struktur Folder

```
masjid/
├── index.php                   
├── api/                       
│   ├── auth.php                
│   ├── reviews.php             
│   ├── facilities.php          
│   ├── gallery.php             
│   └── video.php            
├── assets/
│   ├── css/style.css           
│   └── js/
│       ├── controller.js       
│       ├── vue-prayer.js       
│       └── vue-reviews.js      
├── includes/
│   └── config.php              
├── views/
│   ├── detail.php              
│   ├── ulasan.php             
│   ├── login.php               
│   └── admin/
│       ├── dashboard.php
│       ├── kelola_fasilitas.php
│       ├── kelola_galeri.php
│       ├── kelola_ulasan.php
│       ├── kelola_video.php
│       ├── _sidebar.php
│       └── _footer.php
│       └── aksi_edit.php
└── uploads/                    
    ├── facilities/
    ├── gallery/
    └── reviews/
```

---
## Dokumentasi Website

### Tampilan Website Publik

- Beranda Utama
<img width="1381" height="7013" alt="beranda utama" src="https://github.com/user-attachments/assets/1e1ecb19-038a-4250-a834-93b29c3be592" />

---

- Detail & Fasilitas
<img width="1381" height="7010" alt="detail   fasilitas" src="https://github.com/user-attachments/assets/4cc92ca1-9ffb-4fa7-8ed8-34a45ce3abd7" />

---

- Ulasan
<img width="1381" height="6586" alt="ulasan" src="https://github.com/user-attachments/assets/43c661ce-a55a-400e-8f1d-2ae5aa20b224" />

---

### Tampilan Halaman Admin
- Halaman Dashboard Admin
<img width="1919" height="969" alt="Screenshot 2026-04-29 224909" src="https://github.com/user-attachments/assets/e6f508f1-a184-45e7-a8eb-9a1aac4bf27f" />

---

- Kelola Ulasan
<img width="1919" height="969" alt="image" src="https://github.com/user-attachments/assets/31dbaed0-2b73-4c5c-974e-3b62321568b4" />
<img width="1919" height="969" alt="image" src="https://github.com/user-attachments/assets/8639008c-5002-44f6-b6a2-924af2b9d618" />
<img width="1918" height="969" alt="image" src="https://github.com/user-attachments/assets/f96db8b1-7377-4eae-b57d-9f2f1e05c2ba" />

---

- Kelola Fasilitas
<img width="1919" height="972" alt="image" src="https://github.com/user-attachments/assets/b9bb594e-a222-4bd0-8e8a-f6f8c5266f1e" />

---

- Kelola Galeri & Video
<img width="1919" height="967" alt="image" src="https://github.com/user-attachments/assets/10f12044-20c5-496d-a9c6-273438a41c88" />
<img width="1919" height="971" alt="image" src="https://github.com/user-attachments/assets/c141113e-133a-4a0e-af26-6add1e45db3d" />



