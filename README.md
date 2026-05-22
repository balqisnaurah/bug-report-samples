# Bug Report Samples

Kumpulan contoh bug report profesional dan bug tracking log untuk pengujian aplikasi web toko online. Mencakup dokumentasi bug dari penemuan hingga verifikasi perbaikan.

---

## Daftar File

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

### `BUG_TRACKING_LOG.md`

Log progres tracking bug dari pertama kali ditemukan hingga selesai diperbaiki dan diverifikasi.

**Isi Bug Tracking Log:**
- Status tracking semua bug (Open, In Progress, Resolved, Closed)
- Tanggal reported, fixed, dan verified
- Assignee untuk setiap bug
- Statistik bug berdasarkan status dan severity
- Average time to fix per severity
- Definisi status dan SLA penyelesaian

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

| Severity | Definisi | SLA Penyelesaian | Contoh |
|----------|----------|------------------|--------|
| Critical | Bug yang menghentikan fungsi utama aplikasi | 24 jam | Data tidak terupdate, sistem crash |
| High | Bug yang sangat mengganggu user experience | 3 hari kerja | Tombol tidak berfungsi, fitur utama error |
| Medium | Bug yang mengganggu tapi ada workaround | 1 minggu | Validasi kurang ketat, gambar tidak optimal |
| Low | Bug minor yang tidak mengganggu fungsi | 2 minggu | Pesan error tidak hilang otomatis |

---

## Ringkasan Statistik

| Severity | Jumlah | Persentase |
|----------|--------|------------|
| Critical | 1 | 20% |
| High | 1 | 20% |
| Medium | 2 | 40% |
| Low | 1 | 20% |
| **Total** | **5** | **100%** |

---

## Bug Lifecycle

```
Open → In Progress → Resolved → Closed
              ↓
          Reopened (jika muncul lagi)
              ↓
          Rejected (jika bukan bug)
```

---

## Tentang

Proyek ini dibuat sebagai bagian dari proses belajar Quality Assurance, khususnya dalam mendokumentasikan, melaporkan, dan tracking bug secara profesional. Setiap bug report ditulis dengan detail yang cukup agar developer bisa langsung memahami masalah dan mereproduksi bug tanpa perlu komunikasi tambahan. Bug tracking log mendemonstrasikan kemampuan mengelola siklus hidup bug dari penemuan hingga verifikasi.
