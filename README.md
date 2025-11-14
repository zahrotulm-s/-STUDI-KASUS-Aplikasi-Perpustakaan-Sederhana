# -STUDI-KASUS-Aplikasi-Perpustakaan-Sederhana
Deskripsi Singkat  Kamu diminta membuat aplikasi berbasis teks untuk mengelola data buku di perpustakaan. Aplikasi ini menggunakan function untuk menambah buku, mencari buku, menampilkan daftar buku, dan menghapus buku.

# List untuk menyimpan data buku
daftar_buku = []

# Function untuk menambah buku
def tambah_buku(judul, penulis, tahun):
    buku = {
        "judul": judul,
        "penulis": penulis,
        "tahun": tahun
    }
    daftar_buku.append(buku)
    print("Buku berhasil ditambahkan!")

# Function untuk menampilkan semua buku
def tampilkan_buku():
    if len(daftar_buku) == 0:
        print("Belum ada buku tersimpan.")
    else:
        print("\nDaftar Buku:")
        for i, buku in enumerate(daftar_buku, start=1):
            print(f"{i}. {buku['judul']} - {buku['penulis']} ({buku['tahun']})")
    print()

# --- Contoh pemanggilan function ---
tambah_buku("Algoritma dan Pemrograman PROPHETIC LEADERSHIP & MANAGEMENT WISDOM ( PROLM )", "Syafii Antonio", 2013)
tambah_buku("Ensiklopedia PERSONAL EXCELLENCE by Integral Application of SHIDDIQ", "Syaii Antonio", 2013)

tampilkan_buku()

