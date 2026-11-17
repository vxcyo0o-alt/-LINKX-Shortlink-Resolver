# LINKX — Shortlink Resolver

Backend Node.js + halaman web responsif untuk memeriksa redirect HTTP/HTTPS.

## Deploy gratis di Render

1. Buat repository baru di GitHub.
2. Upload seluruh isi folder proyek ini ke repository (jangan upload `node_modules`).
3. Buka https://render.com dan login.
4. Pilih **New +** → **Blueprint**.
5. Hubungkan repository GitHub tadi.
6. Render membaca `render.yaml`; pilih deploy.
7. Tunggu build selesai, lalu buka URL `.onrender.com` yang diberikan Render.

## Jalankan lokal

Butuh Node.js 20 atau lebih baru.

```bash
npm install
npm start
```

Buka `http://localhost:3000`.

## Batasan dan keamanan

- Hanya mengikuti redirect HTTP 301/302/303/307/308.
- Maksimal 10 redirect dan timeout 10 detik per hop.
- Menolak localhost, IP privat, dan alamat IP khusus.
- Tidak mengeksekusi JavaScript halaman, CAPTCHA, login, survei, atau alur iklan.
- Sebagian layanan shortlink memerlukan cookie, JavaScript, atau interaksi manusia sehingga tidak dapat diselesaikan oleh pemeriksa redirect ini.
- Ini alat pemeriksa redirect, bukan layanan untuk menghindari kontrol akses atau kewajiban situs.
