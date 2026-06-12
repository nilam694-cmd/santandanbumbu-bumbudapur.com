# Santan & Bumbu Dapur – Website UMKM

Website statis siap hosting di **GitHub Pages**.

## Struktur Folder

```
/
├── index.html
├── README.md
└── assets/
    ├── images/   (15 file .webp, total ±624 KB)
    ├── css/
    │   └── style.css
    └── js/
        └── script.js
```

Total ukuran project: **±736 KB** (jauh di bawah batas 25 MB).

## Optimasi yang Dilakukan

1. Semua gambar (sebelumnya disisipkan sebagai base64 di HTML, total ±20 MB)
   diekstrak, dikompres, dan dikonversi ke format **WebP**.
2. CSS dan JavaScript dipisah ke file `.css` dan `.js` tersendiri agar
   browser dapat melakukan caching dan loading lebih cepat.
3. Duplikat gambar dihapus (gambar yang sama dipakai ulang).
4. Ditambahkan `meta description` dan `preconnect` untuk Google Fonts agar
   loading lebih optimal.
5. Tampilan, layout, warna, dan animasi **tidak diubah** — desain tetap
   identik dengan versi asli.
6. Website sudah responsive untuk desktop, tablet, dan mobile (media query
   sudah diuji dan tetap berfungsi).

## Cara Aktivasi GitHub Pages

1. Buat repository baru di GitHub (contoh: `santan-bumbu-dapur`).
2. Upload seluruh isi folder ini (jangan upload folder pembungkusnya, cukup
   isi: `index.html`, `README.md`, dan folder `assets/`) ke repository
   tersebut — bisa lewat web GitHub (drag & drop) atau via Git:

   ```bash
   git init
   git add .
   git commit -m "Initial commit - Santan & Bumbu Dapur website"
   git branch -M main
   git remote add origin https://github.com/USERNAME/santan-bumbu-dapur.git
   git push -u origin main
   ```

3. Di repository, buka **Settings → Pages**.
4. Pada bagian **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: pilih **main** dan folder **/(root)**
   - Klik **Save**.
5. Tunggu 1–2 menit, GitHub akan menampilkan URL website Anda, formatnya:

   ```
   https://USERNAME.github.io/santan-bumbu-dapur/
   ```

   (ganti `USERNAME` dengan username GitHub Anda dan
   `santan-bumbu-dapur` dengan nama repository Anda).

6. Buka URL tersebut — website akan langsung tampil dan berfungsi penuh
   (navigasi, slider produk, modal resep, FAQ accordion, dan tombol
   WhatsApp semuanya aktif).

## Catatan

- Pastikan nama file `index.html` tidak diubah — GitHub Pages mencari file
  ini sebagai halaman utama secara otomatis.
- Jika ingin menggunakan custom domain, tambahkan file `CNAME` berisi nama
  domain Anda di root repository, lalu atur DNS sesuai dokumentasi GitHub
  Pages.
