# 📘 Software Design Document (SDD)
**Nama Proyek**: Sistem Informasi Layanan Akademik  
**Universitas**: Universitas Muhammadiyah Bima  
**Versi**: 1.0  
**Tanggal**: 20 Mei 2025  
**Penulis**: [tika nani]

---

## 1. Pendahuluan

### 1.1 Tujuan
Dokumen ini menjelaskan desain teknis dari Sistem Informasi Layanan Akademik yang mencakup arsitektur sistem, desain basis data, dan alur proses.

### 1.2 Lingkup
Sistem ini dirancang untuk melayani kebutuhan akademik mahasiswa, dosen, dan admin, termasuk pengajuan surat, notifikasi akademik, dan sistem pengaduan.

### 1.3 Definisi, Akronim, dan Singkatan
- **SDD**: Software Design Document  
- **SI**: Sistem Informasi  
- **UI**: User Interface  
- **DB**: Database  

---

## 2. Deskripsi Umum Sistem

### 2.1 Arsitektur Sistem
Sistem dibangun dengan:
- **Frontend**: Blade Template Laravel
- **Backend**: Laravel 10 (PHP)
- **Database**: MySQL
- **Deployment**: Hosting/VPS + GitHub

### 2.2 Pengguna Sistem
- **Admin**: Mengelola data, verifikasi surat, input pengumuman
- **Dosen**: Membaca pengumuman, memberi respon konsultasi
- **Mahasiswa**: Mengajukan surat, melihat notifikasi, membuat pengaduan

---

## 3. Desain Sistem

### 3.1 Use Case Diagram
_(Use case diagram diletakkan di sini atau dijelaskan link-nya jika berupa gambar)_

### 3.2 Desain Database (ERD)
_(Deskripsikan tabel utama: users, surat, pengaduan, notifikasi, dll)_

Contoh:
- **users**: id, nama, email, password, role
- **surat**: id, user_id, jenis_surat, status, tanggal_pengajuan

### 3.3 Alur Sistem (Flowchart / Activity Diagram)
- Login → Dashboard → Akses modul (surat/pengaduan/notifikasi)

---

## 4. Desain Antarmuka (UI)

### 4.1 Halaman Login
- Form dengan role selection (Admin, Dosen, Mahasiswa)

### 4.2 Halaman Dashboard
- Ditampilkan berdasarkan role pengguna.

### 4.3 Form Pengajuan Surat
- Field: Jenis surat, keperluan, file lampiran (opsional)

---

## 5. Komponen dan Modul

| Modul                 | Deskripsi Singkat                                      |
|----------------------|--------------------------------------------------------|
| Login & Auth         | Login berdasarkan role dan session                     |
| Modul Surat          | Pengajuan dan verifikasi surat mahasiswa               |
| Modul Pengumuman     | Input & tampilkan pengumuman untuk semua pengguna      |
| Modul Pengaduan      | Mahasiswa buat pengaduan, admin kelola                 |
| Modul Konsultasi     | Interaksi dosen–mahasiswa dalam bentuk chat/tanggapan  |

---

## 6. Keamanan Sistem

- Hashing password dengan bcrypt
- Validasi role akses (middleware)
- Sanitasi input dari user (request validation)

---

## 7. Deployment

- Project dikelola melalui GitHub
- Commit rutin disertai pesan meaningful
- Dideploy ke server hosting / VPS via FTP atau CI/CD GitHub

---

## 8. Referensi

- Dokumentasi Laravel: https://laravel.com/docs
- Standar SRS/SDD: IEEE 1016-2009
