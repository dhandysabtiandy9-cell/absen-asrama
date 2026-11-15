# Absen SRT2

Sistem absensi asrama berbasis web (HTML + JavaScript) dengan **Supabase** (database, login, penyimpanan foto) dan **Vercel** (hosting).

## Fitur
- Absensi harian sekolah, sholat 5 waktu, dan ibadah (per agama)
- Penilaian kebersihan kamar dengan foto bukti
- Laporan kebutuhan khusus siswa dan rekap pemantauan
- Rekap absensi, pengumuman, dan manajemen data siswa
- Dua peran: **admin** dan **wali** (akun dibuat admin lewat `api/wali.js`)

## Teknologi
HTML, CSS, JavaScript, Supabase (PostgreSQL, Auth, Storage, RLS), Vercel Serverless Function, Chart.js

## Cara menjalankan
1. Buat project Supabase, jalankan `supabase/schema.sql` di SQL Editor, matikan *Allow new users to sign up*.
2. Buat user pertama (otomatis jadi admin), lalu isi `url` dan `anonKey` di `assets/js/config.js`.
3. Deploy ke Vercel dan isi Environment Variables: `SUPABASE_URL`, `SUPABASE_SERVICE_ROLE_KEY`, `EMAIL_DOMAIN` (opsional).

## Struktur
```
├── *.html            # halaman (login, absen, rekap, kebersihan, dll.)
├── assets/css/style.css
├── assets/js/        # app.js, config.js
├── api/wali.js       # fungsi server kelola akun wali
├── supabase/schema.sql
└── package.json
```
