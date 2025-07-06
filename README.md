# 🔧 Laravel Custom Helpers

Kumpulan fungsi helper global untuk mempercepat pengembangan aplikasi Laravel.  
File ini berisi utilitas tambahan untuk manipulasi tanggal, string, angka, format, dan lainnya.

---

## 📁 Struktur

File helper ini berisi lebih dari **40+ fungsi siap pakai**, yang dikelompokkan berdasarkan kategori:

---

## 📆 Tanggal & Waktu

| Fungsi              | Deskripsi                                                                 |
|---------------------|---------------------------------------------------------------------------|
| `increment_workday` | Tambah hari kerja ke tanggal tertentu, lewati weekend & hari libur       |
| `list_dates`        | Daftar tanggal dalam bulan & tahun tertentu                               |
| `list_full_dates`   | Sama seperti `list_dates` + nama hari                                     |
| `list_hari`         | Daftar nama hari (Senin - Minggu)                                         |
| `fulldate`          | Format tanggal ke bentuk tulisan: `Rabu, 10 Juli 2025`                    |
| `format_date`       | Format `Y-m-d` ke `d-m-Y` (atau custom)                                   |
| `format_time`       | Format waktu ke `H:i` atau `H:i:s`                                        |
| `date_difference`   | Hitung jumlah hari antara dua tanggal                                     |
| `unformat_date`     | Format ulang ke `Y-m-d`                                                   |
| `todayDate`         | Ambil tanggal hari ini (`Y-m-d`)                                          |
| `isToday`           | Cek apakah tanggal adalah hari ini                                        |

---

## 🔢 Angka & Format

| Fungsi               | Deskripsi                                                                |
|----------------------|-------------------------------------------------------------------------|
| `format_number`      | Format angka ribuan (misal `10000` → `10.000`)                          |
| `format_decimal`     | Format angka dengan koma/titik sesuai locale                            |
| `format_decimal2`    | Format angka dengan 4 digit desimal                                     |
| `number_to_alphabeth`| Ubah angka ke huruf (1 = A, 2 = B, dst)                                 |
| `number_to_roman`    | Angka ke Romawi (`4 → IV`)                                               |
| `roman_to_number`    | Romawi ke angka (`IV → 4`)                                               |
| `spell_number`       | Ubah angka menjadi huruf (`123 → seratus dua puluh tiga`)               |
| `unformat_number`    | Hapus pemisah ribuan & ubah ke float                                    |

---

## 🔤 String Utilities

| Fungsi         | Deskripsi                                                  |
|----------------|-------------------------------------------------------------|
| `str_limit`    | Potong string (`Str::limit`)                                |
| `str_slug`     | Buat slug dari teks (`Str::slug`)                           |
| `str_unslug`   | Ubah slug jadi teks biasa (`halo-dunia` → `Halo Dunia`)     |
| `str_plural`   | Bentuk jamak string (`Str::plural`)                         |
| `remove_space` | Hapus semua spasi                                           |
| `serialize_array` | Ubah array ke query string (`http_build_query`)          |

---

## 📥 Dropdown / Pilihan Data

| Fungsi           | Deskripsi                                        |
|------------------|---------------------------------------------------|
| `unit_durations` | Pilihan unit waktu (`Days`, `Weeks`, dst.)       |
| `paginate_options` | Opsi per halaman (`10`, `20`, `50`, `100`)      |
| `gender`         | Pilihan jenis kelamin (`L`, `P`)                 |
| `religion`       | Pilihan agama                                    |
| `list_bulan`     | Nama bulan (`Januari` s/d `Desember`)            |

---

## 🌐 Routing & Utilitas Lain

| Fungsi      | Deskripsi                                                        |
|-------------|-------------------------------------------------------------------|
| `has_route` | Cek apakah route tersedia & kembalikan URL-nya atau `#`          |

---

## ✅ Cara Menggunakan

1. Simpan file ini di: `app/Helpers/global.php`
2. Tambahkan ke `composer.json`:
```json
"autoload": {
    "files": [
        "app/Helpers/global.php"
    ]
}
