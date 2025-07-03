# 📊 internSIG_mergeprod

> Automatisasi penggabungan laporan produksi harian Kiln 1-4 dari file Excel bulanan PT Semen Indonesia

---

## 🔍 Deskripsi
Script Python ini dibuat untuk **menggabungkan data produksi kiln** dari file Excel bulanan `Tuban kiln operation report` yang tersebar dalam subfolder berdasarkan bulan (`JAN`, `PEB`, dll). File diekstrak secara otomatis berdasarkan struktur nama file `Tuban kiln operation report MM-YYYY.xlsx`, tanpa perlu menyalin path satu per satu.

---

## 📁 Struktur Folder Input
admpbp - PRODUKSI/
├── JAN/
│ └── Tuban kiln operation report 01-2025.xlsx
├── FEB/
│ └── Tuban kiln operation report 02-2025.xlsx


---

## ✅ Fitur Utama
- 🔄 Membaca otomatis semua file dengan pola nama `Tuban kiln operation report MM-YYYY.xlsx`.
- 📅 Menghitung jumlah hari per bulan dengan `calendar`.
- 📑 Memproses keempat sheet: `Kiln 1`, `Kiln 2`, `Kiln 3`, `Kiln 4`.
- 🧹 Otomatis membuang file yang tidak sesuai format atau dari folder tidak relevan.
- 📦 Menyimpan hasil gabungan sebagai satu file `.xlsx`.

---
## 📦 Kebutuhan Library

| Library     | Keterangan                                                                 |
|-------------|-----------------------------------------------------------------------------|
| `pandas`    | Untuk membaca dan menggabungkan data dari file Excel (`pd.read_excel`)     |
| `calendar`  | Untuk menghitung jumlah hari dalam setiap bulan                            |
| `os`        | Untuk navigasi folder dan file otomatis (`os.listdir`, `os.path`)          |
| `re`        | Untuk validasi nama file menggunakan pola regex                            |
| `openpyxl`  | Digunakan oleh pandas untuk membaca file `.xlsx`                           |
