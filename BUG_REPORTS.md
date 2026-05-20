\# Bug Report - Toko Online v1.0



\*\*Reporter:\*\* Balqis Naurah Hanifah  

\*\*Environment:\*\* Windows 11, Chrome 130, Resolusi 1920x1080  



\---



\## BUG-001: Tombol "Tambah ke Keranjang" tidak responsif pada mobile



| Field | Detail |

|-------|--------|

| \*\*Bug ID\*\* | BUG-001 |

| \*\*Severity\*\* | High |

| \*\*Priority\*\* | High |

| \*\*Status\*\* | Open |

| \*\*Modul\*\* | Produk |

| \*\*Browser\*\* | Chrome Mobile (Android 14) |

| \*\*Resolusi\*\* | 360x800 |



\*\*Deskripsi:\*\*  

Tombol "Tambah ke Keranjang" pada halaman detail produk tidak dapat diklik pada perangkat mobile. Tombol terlihat normal tetapi tidak merespons sentuhan.



\*\*Langkah Reproduksi:\*\*  

1\. Buka halaman produk di perangkat mobile (atau Chrome DevTools mode responsive)

2\. Pilih salah satu produk

3\. Di halaman detail produk, coba tap tombol "Tambah ke Keranjang"



\*\*Expected Result:\*\*  

Produk berhasil ditambahkan ke keranjang dan muncul notifikasi konfirmasi.



\*\*Actual Result:\*\*  

Tombol tidak merespons sentuhan. Tidak ada produk yang ditambahkan ke keranjang.



\*\*Root Cause (Dugaan):\*\*  

Elemen overlay atau z-index yang menutupi tombol pada viewport mobile.



\---



\## BUG-002: Harga total tidak terupdate saat mengubah quantity



| Field | Detail |

|-------|--------|

| \*\*Bug ID\*\* | BUG-002 |

| \*\*Severity\*\* | Critical |

| \*\*Priority\*\* | Critical |

| \*\*Status\*\* | Open |

| \*\*Modul\*\* | Keranjang |

| \*\*Browser\*\* | Chrome 130, Firefox 131 |



\*\*Deskripsi:\*\*  

Ketika user mengubah quantity produk di keranjang, harga total di bagian summary tidak terupdate secara otomatis. Harga baru muncul setelah halaman di-refresh manual.



\*\*Langkah Reproduksi:\*\*  

1\. Tambahkan produk ke keranjang

2\. Buka halaman keranjang

3\. Ubah quantity dari 1 menjadi 3

4\. Perhatikan total harga di bagian Order Summary



\*\*Expected Result:\*\*  

Total harga otomatis berubah menjadi harga satuan x 3.



\*\*Actual Result:\*\*  

Total harga masih menampilkan harga untuk quantity 1. Baru berubah setelah refresh halaman.



\*\*Root Cause (Dugaan):\*\*  

Event listener pada input quantity tidak memicu recalculation total harga secara real-time.



\---



\## BUG-003: Pesan error login tidak menghilang setelah input diperbaiki



| Field | Detail |

|-------|--------|

| \*\*Bug ID\*\* | BUG-003 |

| \*\*Severity\*\* | Low |

| \*\*Priority\*\* | Low |

| \*\*Status\*\* | Open |

| \*\*Modul\*\* | Login |

| \*\*Browser\*\* | Semua browser |



\*\*Deskripsi:\*\*  

Pesan error "Email atau password salah" tetap muncul meskipun user sudah memperbaiki input dan belum menekan tombol Login lagi.



\*\*Langkah Reproduksi:\*\*  

1\. Buka halaman login

2\. Masukkan email valid dan password salah

3\. Klik Login (muncul pesan error)

4\. Perbaiki password tanpa klik Login



\*\*Expected Result:\*\*  

Pesan error hilang saat user mulai mengetik ulang di field input.



\*\*Actual Result:\*\*  

Pesan error tetap muncul sampai user klik Login lagi.



\---



\## BUG-004: Gambar produk tidak muncul pada koneksi lambat



| Field | Detail |

|-------|--------|

| \*\*Bug ID\*\* | BUG-004 |

| \*\*Severity\*\* | Medium |

| \*\*Priority\*\* | Medium |

| \*\*Status\*\* | Open |

| \*\*Modul\*\* | Produk |

| \*\*Browser\*\* | Semua browser |



\*\*Deskripsi:\*\*  

Gambar produk menampilkan ikon broken image saat diakses pada koneksi internet lambat (3G). Tidak ada placeholder atau lazy loading yang diterapkan.



\*\*Langkah Reproduksi:\*\*  

1\. Buka Chrome DevTools

2\. Di tab Network, set throttling ke "Slow 3G"

3\. Buka halaman katalog produk

4\. Perhatikan gambar produk



\*\*Expected Result:\*\*  

Gambar menampilkan placeholder loading terlebih dahulu, lalu gambar muncul setelah selesai dimuat.



\*\*Actual Result:\*\*  

Gambar langsung menampilkan ikon broken image. Beberapa gambar baru muncul setelah beberapa detik tanpa indikasi loading.



\---



\## BUG-005: Form checkout tidak memvalidasi nomor telepon



| Field | Detail |

|-------|--------|

| \*\*Bug ID\*\* | BUG-005 |

| \*\*Severity\*\* | Medium |

| \*\*Priority\*\* | High |

| \*\*Status\*\* | Open |

| \*\*Modul\*\* | Checkout |

| \*\*Browser\*\* | Semua browser |



\*\*Deskripsi:\*\*  

Field nomor telepon di form checkout menerima input huruf dan karakter spesial tanpa validasi. User bisa submit pesanan dengan nomor telepon yang tidak valid.



\*\*Langkah Reproduksi:\*\*  

1\. Tambahkan produk ke keranjang

2\. Buka halaman checkout

3\. Di field nomor telepon, masukkan "abcdef"

4\. Isi field lainnya dengan data valid

5\. Klik "Bayar Sekarang"



\*\*Expected Result:\*\*  

Muncul validasi "Nomor telepon harus berupa angka" atau "Format nomor telepon tidak valid".



\*\*Actual Result:\*\*  

Pesanan berhasil dibuat dengan nomor telepon "abcdef".



\---



\## Ringkasan Bug



| Severity | Jumlah | Bug ID |

|----------|--------|--------|

| Critical | 1 | BUG-002 |

| High | 1 | BUG-001 |

| Medium | 2 | BUG-004, BUG-005 |

| Low | 1 | BUG-003 |

| \*\*Total\*\* | \*\*5\*\* | |

