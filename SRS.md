# 📄 Software Requirements Specification (SRS)
**Nama Proyek**: Sistem Informasi Layanan Akademik  
**Universitas**: Universitas Muhammadiyah Bima  
**Versi**: 1.0  
**Tanggal**: 20 Mei 2025  
**Penulis**: [Nama Anda]

---

## 1. Pendahuluan

### 1.1 Tujuan
Dokumen ini bertujuan menjabarkan seluruh kebutuhan perangkat lunak Sistem Informasi Layanan Akademik agar dapat dikembangkan sesuai dengan harapan stakeholder.

### 1.2 Lingkup Sistem
Sistem ini akan melayani kebutuhan layanan akademik berbasis web dengan fitur:
- Login 3 level (admin, dosen, mahasiswa)
- Pengajuan & verifikasi surat
- Notifikasi pengumuman
- Sistem pengaduan & konsultasi

### 1.3 Definisi & Singkatan
- **SRS**: Software Requirements Specification
- **Admin**: Pengelola sistem
- **UI**: User Interface
- **CRUD**: Create, Read, Update, Delete

---

## 2. Deskripsi Umum

### 2.1 Perspektif Sistem
Aplikasi berbasis web terhubung ke basis data MySQL, menggunakan framework Laravel sebagai backend dan Blade untuk frontend.

### 2.2 Fungsi Umum Sistem

| Pengguna     | Fungsi Utama                                               |
|--------------|------------------------------------------------------------|
| Admin        | Verifikasi surat, input pengumuman, kelola data pengguna   |
| Dosen        | Melihat pengumuman, memberi tanggapan konsultasi           |
| Mahasiswa    | Mengajukan surat, melihat status, membuat pengaduan        |

---

## 3. Kebutuhan Fungsional

### 3.1 Login
- Pengguna dapat login sesuai role
- Autentikasi melalui email & password

### 3.2 Pengajuan Surat
- Mahasiswa dapat memilih jenis surat, isi keterangan, dan mengirim
- Admin dapat menerima dan memverifikasi surat

### 3.3 Pengumuman
- Admin dapat membuat dan mengedit pengumuman
- Semua pengguna dapat melihat pengumuman

### 3.4 Pengaduan
- Mahasiswa mengirim pengaduan
- Admin menerima dan merespon

### 3.5 Konsultasi
- Mahasiswa dan dosen/admin dapat bertukar pesan konsultasi

---

## 4. Kebutuhan Non-Fungsional

| Kebutuhan            | Deskripsi                                                                 |
|----------------------|--------------------------------------------------------------------------|
| Keamanan             | Password di-hash dengan bcrypt, validasi role akses                      |
| Kinerja              | Respon cepat (<2 detik per permintaan)                                   |
| Portabilitas         | Dapat diakses melalui browser desktop dan mobile                         |
| Reliabilitas         | Sistem mampu berjalan 24/7 tanpa downtime kritis                         |
| Maintainability      | Kode bersih, terstruktur (Laravel MVC), modular untuk pemeliharaan mudah |

---

## 5. Antarmuka Pengguna

- Halaman login dengan pilihan role
- Dashboard sesuai jenis pengguna
- Navigasi jelas ke modul surat, pengumuman, pengaduan, dan konsultasi

---

## 6. Batasan Sistem

- Akses hanya untuk pengguna terdaftar
- Sistem membutuhkan koneksi internet
- Tidak mendukung pengunggahan file berukuran lebih dari 2MB

---

## 7. Use Case Diagram
_(Tambahkan diagram jika ada, atau deskripsikan secara tertulis)_

Contoh:
- Mahasiswa → Login → Ajukan Surat → Lihat Status
- Admin → Login → Verifikasi Surat → Input Pengumuman
- Dosen → Login → Balas Konsultasi

---

## 8. Spesifikasi Hardware & Software

| Kategori       | Spesifikasi Minimal                                  |
|----------------|------------------------------------------------------|
| Browser        | Chrome/Firefox terbaru                               |
| Server         | PHP ≥ 8.1, MySQL ≥ 5.7, Composer, Laravel CLI        |
| Client         | Perangkat dengan akses internet dan browser modern  |

---

## 9. Referensi

- Standar IEEE 830-1998 untuk SRS
- Laravel Documentation: https://laravel.com/docs
