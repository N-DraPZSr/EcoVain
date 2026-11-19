# Requirements Platform EcoVein

## Studi Kasus

| Komponen | Keterangan |
|---|---|
| Platform | Eco-Green |
| Pengguna sasaran | Masyarakat umum dari berbagai kalangan dan usia |
| Situasi penggunaan | Membuka website dari ponsel atau komputer untuk mencari informasi lingkungan, berdonasi, atau mendaftar relawan |
| Kebutuhan pengguna | Informasi lingkungan yang mudah dipahami, donasi aman, pendaftaran relawan, dan pemantauan transparansi dana |
| Tujuan platform | Pusat informasi lingkungan yang terpercaya dan mendorong partisipasi aktif masyarakat |
| Tindakan utama | Membaca edukasi, membuat akun, mengisi formulir donasi, mendaftar relawan, memantau dashboard transparansi |
| Ruang lingkup | Beranda, edukasi, donasi, relawan, transparansi, login/register, panel admin, database |
| Di luar ruang lingkup | Payment gateway otomatis (QRIS), notifikasi email/push, fitur chat, aplikasi mobile native |

---

## Kebutuhan Fungsional

| ID | Kebutuhan | Kriteria Penerimaan |
|---|---|---|
| F-01 | Pengguna dapat membaca konten edukasi lingkungan | Halaman edukasi menampilkan minimal 4 topik: zero waste, waste management, konservasi alam, perubahan iklim |
| F-02 | Pengguna dapat mendaftar akun | Formulir registrasi memuat nama, email, kata sandi; data tersimpan di database |
| F-03 | Pengguna dapat login | Formulir login memverifikasi email dan kata sandi; sesi aktif setelah berhasil masuk |
| F-04 | Pengguna yang sudah login dapat mengisi formulir donasi | Formulir donasi hanya bisa diakses setelah login; data tersimpan di database |
| F-05 | Pengguna yang sudah login dapat mendaftar sebagai relawan | Formulir relawan hanya bisa diakses setelah login; data tersimpan di database |
| F-06 | Pengguna dapat melihat dashboard transparansi | Dashboard menampilkan total donasi, daftar kegiatan, dan ringkasan penggunaan dana |
| F-07 | Admin dapat masuk ke panel admin | Login admin terpisah; hanya akun admin yang bisa mengaksesnya |
| F-08 | Admin dapat mengelola data donatur | Admin dapat melihat, memfilter, dan mengekspor daftar donatur |
| F-09 | Admin dapat mengelola data relawan | Admin dapat melihat, mengonfirmasi, dan menolak pendaftaran relawan |
| F-10 | Admin dapat memperbarui laporan transparansi | Admin dapat menambah, mengedit, dan menghapus entri laporan keuangan dan kegiatan |
| F-11 | Navigasi antar halaman berfungsi dengan benar | Semua tautan menuju halaman yang sesuai; halaman terlindungi redirect ke login jika belum masuk |

---

## Kebutuhan Nonfungsional

| ID | Kebutuhan | Kriteria Penerimaan |
|---|---|---|
| NF-01 | Tampilan responsif | Tidak ada scroll horizontal pada viewport 360 px hingga 1366 px |
| NF-02 | Navigasi dapat digunakan melalui keyboard | Semua tautan dapat difokuskan dan diaktifkan tanpa mouse |
| NF-03 | Keamanan autentikasi | Kata sandi disimpan dalam bentuk hash (bcrypt); sesi menggunakan token aman |
| NF-04 | Keamanan data pengguna | Input divalidasi dan disanitasi untuk mencegah SQL injection dan XSS |
| NF-05 | Markup HTML valid | Tidak ada error saat diperiksa di validator.w3.org |
| NF-06 | Proyek mudah dipelihara | CSS terpisah dari HTML, kode backend terstruktur, dan README tersedia |

---

## Kebutuhan Teknis

- Viewport uji: 360 px, 390 px, 768 px, 1366 px
- Peramban uji: Google Chrome dan Mozilla Firefox
- Frontend: HTML, CSS, JavaScript tanpa framework CSS
- Backend: Node.js / PHP dengan database MySQL / PostgreSQL
- Autentikasi: JWT / session cookie + enkripsi bcrypt
