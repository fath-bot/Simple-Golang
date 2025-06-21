# Sistem Manajemen Inventori Barang

Sebuah sistem manajemen inventori sederhana yang dibuat dengan bahasa Go untuk mengelola produk, mencatat transaksi.
Project Tugas Semester 2

## Fitur Utama

- **Manajemen Produk**:
  - Tambah produk baru
  - Ubah data produk yang ada
  - Hapus produk
  - Lihat daftar produk

- **Pencatatan Transaksi**:
  - Mencatat semua perubahan stok
  - Melacak penambahan, perubahan, dan penghapusan
  - Pencatatan waktu transaksi

- **Fitur Pencarian**:
  - Cari produk berdasarkan nama
  - Cari produk berdasarkan harga
  - Cari produk berdasarkan stok
  - Filter transaksi berdasarkan jenis, tanggal, atau nilai

- **Pengurutan dan Laporan**:
  - Urutkan produk berdasarkan harga atau stok
  - Urutkan transaksi berdasarkan tanggal atau nilai
  - Opsi pengurutan naik (ascending) dan turun (descending)

## Struktur Data

Program ini menggunakan 3 struktur data utama:

1. `dataBarang` (Produk):
   - `namaBarang`: Nama produk (string)
   - `harga`: Harga produk (int)
   - `stok`: Jumlah stok (int)

2. `dataTransaksi` (Transaksi):
   - `namaBarang`: Nama produk (string)
   - `jenis`: Jenis transaksi ("tambah", "ubah", "hapus")
   - `waktu`: Tanggal transaksi (struct date)
   - `nilai`: Perubahan nilai (int)
   - `jumlahWaktu`: Tanggal dalam hari (untuk pengurutan)

3. `date` (Tanggal):
   - `tanggal`: Tanggal (int)
   - `bulan`: Bulan (int)
   - `tahun`: Tahun (int)

## Cara Menggunakan

1. **Menjalankan Program**:
   - Pastikan Go sudah terinstall
   - Clone repository ini
   - Jalankan `go run main.go`

2. **Menu Utama**:
   - **Modifikasi Data**: Tambah, edit, atau hapus produk
   - **Cari Data**: Temukan produk atau transaksi
   - **Tampilan Data**: Tampilkan daftar produk/transaksi yang terurut

3. **Navigasi**:
   - Ikuti petunjuk di layar
   - Gunakan angka untuk memilih opsi
   - Kembali ke menu sebelumnya dengan pilihan "kembali"

## Contoh Penggunaan

1. Menambah produk baru:
   - Pilih "Modifikasi Data" > "Tambah Data"
   - Masukkan nama, harga, dan stok produk
   - Sistem akan otomatis mencatat transaksi

2. Mencari produk:
   - Pilih "Cari Data" > "Cari berdasarkan Nama"
   - Masukkan nama produk untuk melihat detail

3. Melihat transaksi terurut:
   - Pilih "Tampilan Data" > "Transaksi" > "Berdasarkan Waktu" > "Descending"
   - Sistem akan menampilkan transaksi terbaru pertama

## Detail Teknis

- Menggunakan penyimpanan berbasis array dengan ukuran maksimum tetap (NMAX = 2023)
- Mengimplementasikan insertion sort untuk pengurutan data
- Memiliki fungsi pencarian yang komprehensif
- Mencatat semua perubahan dengan timestamp

## Keterbatasan

- Ukuran array tetap membatasi skalabilitas
- Tidak ada penyimpanan persisten (data hilang saat program berakhir)
- Antarmuka konsol dasar

## Pengembangan Selanjutnya

- Menambahkan integrasi database untuk penyimpanan persisten
- Mengimplementasikan algoritma pengurutan yang lebih efisien
- Menambahkan autentikasi pengguna
- Mengembangkan antarmuka grafis
