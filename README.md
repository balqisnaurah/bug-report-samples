# Bug Report Samples

Kumpulan contoh bug report profesional yang ditemukan saat pengujian aplikasi web toko online. Setiap bug didokumentasikan dengan format standar yang umum digunakan dalam industri QA.

---

## Daftar Bug Report

### `BUG_REPORTS.md`

Berisi 5 contoh bug report dengan severity berbeda.

**Daftar Bug:**

| Bug ID | Severity | Modul | Judul |
|--------|----------|-------|-------|
| BUG-001 | High | Produk | Tombol "Tambah ke Keranjang" tidak responsif pada mobile |
| BUG-002 | Critical | Keranjang | Harga total tidak terupdate saat mengubah quantity |
| BUG-003 | Low | Login | Pesan error login tidak menghilang setelah input diperbaiki |
| BUG-004 | Medium | Produk | Gambar produk tidak muncul pada koneksi lambat |
| BUG-005 | Medium | Checkout | Form checkout tidak memvalidasi nomor telepon |

---

## Format Bug Report

Setiap bug report didokumentasikan dengan format standar berikut:

| Field | Deskripsi |
|-------|-----------|
| **Bug ID** | Identifier unik bug (contoh: BUG-001) |
| **Severity** | Tingkat keparahan: Critical, High, Medium, Low |
| **Priority** | Prioritas perbaikan |
| **Status** | Open, In Progress, Resolved, Closed |
| **Modul** | Bagian aplikasi yang terkena dampak |
| **Browser** | Browser dan versi yang digunakan saat pengujian |
| **Deskripsi** | Penjelasan singkat tentang bug |
| **Langkah Reproduksi** | Step-by-step cara mereproduksi bug |
| **Expected Result** | Hasil yang seharusnya terjadi |
| **Actual Result** | Hasil yang sebenarnya terjadi |
| **Root Cause** | Dugaan penyebab bug (jika ada) |

---

## Klasifikasi Severity

| Severity | Definisi | Contoh |
|----------|----------|--------|
| Critical | Bug yang menghentikan fungsi utama aplikasi | Data tidak terupdate, sistem crash |
| High | Bug yang sangat mengganggu user experience | Tombol tidak berfungsi, fitur utama error |
| Medium | Bug yang mengganggu tapi ada workaround | Validasi kurang ketat, gambar tidak optimal |
| Low | Bug minor yang tidak mengganggu fungsi | Pesan error tidak hilang otomatis |

---

## Ringkasan Statistik

| Severity | Jumlah |
|----------|--------|
| Critical | 1 |
| High | 1 |
| Medium | 2 |
| Low | 1 |
| **Total** | **5** |

---

## Tentang

Proyek ini dibuat sebagai bagian dari proses belajar Quality Assurance, khususnya dalam mendokumentasikan dan melaporkan bug secara profesional. Setiap bug report ditulis dengan detail yang cukup agar developer bisa langsung memahami masalah dan mereproduksi bug tanpa perlu komunikasi tambahan.
