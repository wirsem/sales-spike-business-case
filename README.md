# 📊 Analisis Produk Terlaris — Visualisasi Penjualan Bulanan

Proyek analisis data sederhana menggunakan Python untuk mengidentifikasi **5 produk terlaris** berdasarkan total unit terjual per bulan, divisualisasikan dalam bentuk line chart interaktif.

---

## 🗂️ Deskripsi Proyek

Script ini melakukan seluruh pipeline analisis data dari awal hingga visualisasi:

1. **Memuat data** — Membaca dua dataset (`tbl_transaction.csv` dan `tbl_product.csv`) dari sumber eksternal.
2. **Menggabungkan data** — Merge transaksi dengan informasi produk menggunakan `product_id`.
3. **Membersihkan data** — Menangani nilai kosong, duplikasi, dan konversi tipe data.
4. **Agregasi** — Menghitung total unit terjual per produk per bulan.
5. **Visualisasi** — Menampilkan tren penjualan 5 produk terlaris dalam line chart.

---

## 📁 Struktur Dataset

### `tbl_transaction.csv`
| Kolom | Keterangan |
|---|---|
| `trx_id` | ID transaksi |
| `trx_date` | Tanggal transaksi (format: DDMMYYYY) |
| `product_id` | ID produk |
| `units` | Jumlah unit terjual |

### `tbl_product.csv`
| Kolom | Keterangan |
|---|---|
| `product_id` | ID produk |
| `product_name` | Nama produk |
| `product_category` | Kategori produk |
| `product_cost` | Harga pokok produk |
| `product_price` | Harga jual produk |

---

## ⚙️ Persyaratan

Pastikan Python sudah terinstal, lalu install dependensi berikut:

```bash
pip install pandas seaborn matplotlib
```

| Library | Versi Minimum | Fungsi |
|---|---|---|
| `pandas` | 1.3+ | Manipulasi dan agregasi data |
| `seaborn` | 0.11+ | Visualisasi statistik |
| `matplotlib` | 3.4+ | Rendering grafik |

---

## 🚀 Cara Menjalankan

```bash
python sales_analysis.py
```

Script akan langsung mengunduh data dari Google Cloud Storage dan menampilkan grafik.

---

## 📈 Output

Line chart yang menampilkan **tren penjualan bulanan** untuk 5 produk dengan total unit terjual tertinggi.

- **Sumbu X** — Periode bulan
- **Sumbu Y** — Total unit terjual
- **Warna garis** — Masing-masing mewakili satu produk

---

## 🛠️ Alur Pemrosesan Data

```
CSV Transaction  ──┐
                   ├──► Merge ──► Cleaning ──► Agregasi ──► Visualisasi
CSV Product      ──┘
```

Langkah pembersihan data yang dilakukan:
- Konversi `trx_date` ke format datetime (`%d%m%Y`)
- Konversi `units` ke integer (mengisi NaN dengan 0)
- Menghapus baris dengan nilai kosong (`dropna`)
- Menghapus data duplikat (`drop_duplicates`)

---

## 👤 Author
**Wira Tarumta Timothy Sembiring**
- 🔗 [LinkedIn](https://linkedin.com/in/wira-tarumta-timothy-sembiring)
- 🐙 [GitHub](https://github.com/wirsem)