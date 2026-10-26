# FAKTA.ID — Kenali Faktanya, Bukan Sekadar Narasinya

Website statis (HTML/CSS/JS) tampilan website umum (navbar atas, responsif), isi mengikuti prototipe 15 layar: splash, beranda, menu layanan, FAKTA News (+detail, kategori), FAKTA AI (+detail verifikasi klaim), FAKTA Community & Guard (+moderasi), profil, notifikasi, pengaturan, tentang.
Jalankan: buka folder di VS Code, klik kanan index.html, Open with Live Server. Deploy: repo GitHub baru, Settings > Pages > main / root.

## Edit cepat (`js/data.js`)
- `NEWS`, `CAT`: berita & kategori (SAAT INI CONTOH). `CLAIMS`: basis data verifikasi (CONTOH).
- `GUARD`: daftar kata untuk moderasi. `CFG.admin`: email moderator. `CFG.aiEndpoint`: URL backend AI.
- Warna: baris `:root` di `css/style.css`.

## Batasan (jujur)
- **FAKTA AI mode demo**: mencocokkan klaim dengan basis data contoh, BUKAN AI sungguhan. Isi `CFG.aiEndpoint` dengan backend Anda (jangan taruh API key di kode web).
- **Guard = filter kata kunci**, bukan AI; kasus ambigu masuk antrean moderator (menu Profil > Moderasi).
- Berita, hasil verifikasi, dan postingan awal = contoh. Ganti dengan konten dan sumber nyata.
- Data (akun, komentar, like) di localStorage (kunci `fk_`) = demo; produksi butuh backend dan pengecekan hak akses di server.
- Belum ada: foto berita, reset password, verifikasi akun, pengikut/mengikuti.

## Menambah gambar
1. Permanen (disarankan): taruh file di `img/`, lalu di `js/data.js` tambahkan `img:"img/nama.jpg"` pada berita. Foto hero beranda: simpan sebagai `img/hero.jpg`.
2. Lewat website: login sebagai admin > Profil > Panel Admin > Tambah Berita (bisa unggah gambar). Disimpan di browser ini saja (demo, kapasitas terbatas).
3. Postingan Community boleh bergambar, tetapi masuk antrean moderator dulu karena gambar tidak bisa dicek otomatis.
