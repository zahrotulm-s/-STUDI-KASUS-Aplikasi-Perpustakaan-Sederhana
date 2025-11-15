# 📚 Aplikasi Perpustakaan

Aplikasi Perpustakaan ini dibuat sebagai sistem pengelolaan buku dan peminjaman di perpustakaan. Sistem ini membantu petugas perpustakaan untuk mencatat data buku, data peminjaman, serta memantau kapan buku dipinjam dan dikembalikan. Aplikasi ini cocok digunakan untuk perpustakaan sekolah, kampus, atau untuk pembelajaran dasar pemrograman.

## 📝 Deskripsi Singkat

Aplikasi ini dirancang untuk mempermudah pencatatan data buku dan transaksi peminjaman. Pengguna dapat melihat daftar buku, menambahkan buku baru, mencatat peminjaman, mengecek status buku (dipinjam / tersedia), dan melihat riwayat peminjaman. Semua data disimpan secara terstruktur sehingga mudah dikelola.

Tujuan utama aplikasi ini adalah:

* Mengurangi pencatatan manual
* Menghindari kehilangan data peminjaman
* Memperkecil risiko buku tidak kembali
* Memberikan pengalaman belajar mengelola database bagi mahasiswa

---

## ✨ Fitur Utama

### 📘 Manajemen Buku

* Menambah data buku baru
* Menampilkan daftar semua buku
* Mengedit atau menghapus data buku
* Menyimpan data seperti:

  * Judul buku
  * Penulis
  * Tahun rilis
  * Kategori
  * Tanggal buku masuk perpustakaan

### 👥 Manajemen Peminjaman

* Mencatat siapa yang meminjam buku
* Menyimpan tanggal pinjam dan tanggal kembali
* Menampilkan daftar peminjaman yang masih berlangsung
* Riwayat peminjaman lengkap

### 🔍 Fitur Pencarian

* Cari buku berdasarkan judul
* Cari berdasarkan penulis
* Cari berdasarkan tahun rilis

---

## 🧱 Desain Database (ERD Sederhana)

**Tabel: `buku`**

| Field         | Tipe Data | Deskripsi                       |
| ------------- | --------- | ------------------------------- |
| id_buku       | INT (PK)  | ID unik buku                    |
| judul         | VARCHAR   | Judul buku                      |
| penulis       | VARCHAR   | Nama penulis                    |
| tahun_rilis   | INT       | Tahun terbit                    |
| tanggal_masuk | DATE      | Tanggal buku masuk perpustakaan |

**Tabel: `peminjaman`**

| Field           | Tipe Data | Deskripsi                            |
| --------------- | --------- | ------------------------------------ |
| id_peminjaman   | INT (PK)  | ID unik peminjaman                   |
| id_buku         | INT (FK)  | Kode buku yang dipinjam              |
| nama_peminjam   | VARCHAR   | Nama orang yang meminjam             |
| tanggal_pinjam  | DATE      | Kapan buku dipinjam                  |
| tanggal_kembali | DATE      | Kapan buku dikembalikan (boleh NULL) |

**Relasi:**

* Satu buku dapat dipinjam berkali-kali → *One to Many*

---

## 📁 Contoh Struktur Folder

```
/aplikasi-perpustakaan
  /src
    /models     -> Struktur data & database
    /views      -> Tampilan UI (jika ada)
    /controllers -> Logika aplikasi
  /database
    database.db / database.sql
  README.md
  app.py / index.js / main.java (sesuaikan)
```

---

## 🧪 Contoh Data (JSON)

### Data Buku

```json
{
  "id_buku": 1,
  "judul": "Belajar Pemrograman",
  "penulis": "Dewi Lestari",
  "tahun_rilis": 2021,
  "tanggal_masuk": "2024-01-10"
}
```

### Data Peminjaman

```json
{
  "id_peminjaman": 1,
  "id_buku": 1,
  "nama_peminjam": "Mufidah",
  "tanggal_pinjam": "2025-01-15",
  "tanggal_kembali": "2025-01-20"
}
```

---

## 🚀 Cara Menjalankan

1. Clone repository

   ```
   git clone https://github.com/username/aplikasi-perpustakaan
   ```
2. Masuk ke folder

   ```
   cd aplikasi-perpustakaan
   ```
3. Jalankan aplikasi

   ```
   python app.py
   ```

   atau

   ```
   npm start
   ```

---

## 🤝 Kontribusi

Silakan berkontribusi dengan cara membuat *pull request*, menambah fitur, atau memberi saran perbaikan.

---

## 📌 Catatan

Aplikasi ini dibuat sebagai tugas mata kuliah **Pemrograman Semester 1** dan dapat dikembangkan lebih lanjut seperti:

* Fitur login admin
* Notifikasi keterlambatan
* Export laporan ke PDF
* Sistem denda
