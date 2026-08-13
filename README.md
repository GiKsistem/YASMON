# YASMON AUTOMOTIVE INDONESIA — Sistem Penjualan (PWA)

Folder ini sudah disiapkan supaya aplikasi HTML kamu bisa:
- di-upload ke GitHub lalu di-hosting gratis (GitHub Pages),
- di-**install jadi aplikasi** di laptop (via Chrome/Edge),
- di-**tambahkan ke Home Screen** di HP (Android/iPhone) seperti app biasa.

## Isi folder
- `index.html` — aplikasi kamu (sudah ditambah dukungan PWA)
- `manifest.json` — info aplikasi (nama, ikon, warna) supaya bisa di-install
- `service-worker.js` — bikin aplikasi tetap bisa dibuka walau tanpa internet
- `icons/` — ikon aplikasi (diambil dari logo Yasmon yang kamu kirim)

## Soal data / backup
Aplikasi ini **tidak** menyimpan data ke server. Data (stok, faktur, dll)
tersimpan sementara di memori browser saat aplikasi dibuka, dan cara
menyimpannya permanen tetap lewat menu **Pengaturan → Download Backup (.json)**
di dalam aplikasi, lalu **Restore Data** untuk memuatnya kembali. Ini tidak
berubah — install sebagai PWA hanya mengubah *cara membukanya* (jadi app),
bukan cara datanya tersimpan. Jadi biasakan backup rutin setelah input data.

## 1. Upload ke GitHub
1. Buat repository baru di GitHub (public), misalnya `yasmon-pos`.
2. Upload semua isi folder ini (`index.html`, `manifest.json`,
   `service-worker.js`, folder `icons/`) ke root repo tersebut.
   - Paling gampang: di halaman repo GitHub klik **Add file → Upload files**,
     lalu drag semua file/folder ini, lalu **Commit changes**.

## 2. Aktifkan GitHub Pages
1. Di repo, buka **Settings → Pages**.
2. Pada **Branch**, pilih `main` (atau `master`) dan folder `/ (root)`, klik **Save**.
3. Tunggu 1–2 menit. GitHub akan kasih link seperti:
   `https://<username-kamu>.github.io/yasmon-pos/`
4. Buka link itu — aplikasi kamu sudah online. **Penting:** aplikasi hanya
   bisa di-install sebagai PWA lewat link `https://...` (harus GitHub Pages
   yang aktif, bukan cuma buka file HTML dari komputer).

## 3. Install sebagai "aplikasi" di laptop
1. Buka link GitHub Pages kamu di **Chrome** atau **Edge**.
2. Di address bar, klik ikon **Install** (biasanya ikon layar/komputer kecil
   di sisi kanan address bar), atau buka menu titik tiga → **Install
   YASMON AUTOMOTIVE INDONESIA...**
3. Aplikasi akan terpasang seperti program biasa: ada ikonnya, bisa dibuka
   dari Start Menu / Desktop, dan terbuka di jendela sendiri (tanpa tab
   browser).

## 4. Tambahkan ke Home Screen di HP
**Android (Chrome):**
1. Buka link GitHub Pages di Chrome.
2. Ketuk menu titik tiga → **Add to Home screen** / **Install app**.
3. Ikon Yasmon akan muncul di layar utama HP.

**iPhone (Safari):**
1. Buka link GitHub Pages di Safari.
2. Ketuk ikon **Share** (kotak dengan panah ke atas).
3. Pilih **Add to Home Screen**.

## Update aplikasi nanti
Kalau kamu ubah `index.html` lagi, upload ulang file yang baru ke repo GitHub
yang sama (replace file). GitHub Pages otomatis update. Karena ada service
worker, kadang perlu **refresh 2x** atau tutup-buka lagi aplikasi supaya versi
terbarunya kepakai.
