# 🛍️ Manajemen Inventaris & Transaksi Pintar untuk Toko Elektronik

## 📌 Latar Belakang

Dalam dunia ritel yang bergerak cepat saat ini, pengelolaan informasi yang efisien menjadi kunci kesuksesan operasional. **Wisantoko Electronic Store**, seperti banyak bisnis kecil hingga menengah lainnya, menghadapi tantangan dalam mengelola data inventaris produk dan transaksi. Pelanggan kerap mengalami keterlambatan akibat informasi stok yang tidak terorganisir dan keterbatasan akses terhadap data produk secara real-time.

Untuk mengatasi permasalahan tersebut, proyek ini mengembangkan sistem **basis data relasional menggunakan MySQL** yang bertujuan mengoptimalkan operasional toko, meningkatkan pengalaman pelanggan, dan merapikan proses internal seperti manajemen stok dan pembuatan nota transaksi.

## 🛠 Metodologi

Tahapan pengembangan proyek meliputi:

1. **Analisis Kebutuhan**
   Mengidentifikasi hambatan operasional, seperti keterlambatan pengecekan stok dan ketidakefisienan proses transaksi.

2. **Perancangan & Normalisasi Basis Data**

   * Mendesain entitas berdasarkan proses bisnis toko: Pelanggan, Produk, Keanggotaan, Pengiriman, Pembayaran, dan sebagainya.
   * Menerapkan **1NF, 2NF, dan 3NF** untuk menghindari redundansi dan menjaga integritas data.

3. **Pembuatan ERD & Skema Relasional**

   * Memodelkan relasi **Many-to-Many** menggunakan tabel penghubung seperti `DetailTransaksi`.
   * Menerapkan relasi **One-to-Many** antar entitas utama (misalnya: Membership → Pelanggan).

4. **Implementasi Trigger**

   * Otomatisasi pengurangan stok saat pembelian atau pengisian ulang.
   * Menjaga konsistensi inventaris (misalnya: sistem akan otomatis menandai produk untuk pengisian ulang jika stok < 20).

5. **Stored Procedure**

   * `generate_invoice` & `generate_invoice_pertransaction`: Membuat nota transaksi lengkap.
   * `calculate_subtotal`: Menghitung total harga termasuk diskon, biaya kirim, dan keuntungan membership.

6. **Query SQL Lanjutan**

   * Mengidentifikasi **produk terlaris dan tidak laku**, serta tren penjualan per bulan.
   * Menyaring penjualan produk berdasarkan bulan tertentu sesuai permintaan.

## 📊 Fitur & Hasil Utama

* **Update Inventaris Real-Time**: Stok otomatis berkurang saat pembelian dan sistem memberi peringatan untuk isi ulang saat stok rendah.
* **Sistem Nota Komprehensif**: Nota mencakup subtotal, diskon, biaya kirim, dan bunga berdasarkan membership.
* **Insight Penjualan**:

  * Produk terlaris: *Samsung Upright Vacuum Cleaner – Orange Sunset*
  * Kategori terendah penjualan: *Refrigerators*
  * Analisis penjualan bulanan secara detail per produk dan per transaksi.
* **Keuntungan Normalisasi**: Menghindari data ganda dan mempermudah pengelolaan data skala besar.
* **Stored Procedure & Trigger Kustom**: Mengurangi input manual, mengotomatisasi perhitungan rutin, dan mencegah inkonsistensi data.

## 📦 Teknologi yang Digunakan

* **Basis Data**: MySQL
* **Desain Data**: Entity-Relationship Diagram (ERD), Normal Forms
* **Fitur SQL**: Views, Stored Procedures, Triggers, Joins, Grouping, Conditional Queries

## 🔍 Contoh Penggunaan

* Seorang kasir mencatat transaksi baru — sistem akan secara otomatis:

  * Mengurangi stok produk,
  * Menghitung subtotal (termasuk diskon),
  * Menambahkan biaya kirim dan bunga berdasarkan membership,
  * Menghasilkan satu baris invoice lengkap untuk pelanggan.
* Manajemen ingin melihat laporan penjualan bulan ini — sistem:

  * Menampilkan semua produk yang terjual,
  * Menyoroti produk dengan performa rendah,
  * Memicu pengisian ulang stok secara otomatis untuk produk yang hampir habis.

## 📎 Akses Data

🔗 [Dataset Mentah & Skrip SQL](https://github.com/ilhamramadhan-m/ElectronicStore-DataManagement/blob/main/Electronic%20Store's%20Selling%20RDBMS.xlsx)
