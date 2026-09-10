# Oliv Propolis

Oliv Propolis adalah aplikasi web statis dengan fitur toko, keranjang, checkout WhatsApp/Midtrans, akun customer, dashboard seller, portal admin, kode referral, dan bantuan AI.

## Struktur

```text
oliv-propolis/
├── index.html
├── package.json
├── assets/
│   ├── css/styles.css
│   ├── js/app.js
│   └── img/
└── README.md
```

## Menjalankan

Tanpa instalasi:

```bash
npx vite --host 0.0.0.0
```

Atau buka `index.html` melalui web server statis. Menjalankan lewat `http://localhost` lebih disarankan agar clipboard dan Supabase bekerja konsisten.

## Catatan konfigurasi

- Pengaturan Supabase, Midtrans, dan endpoint fungsi tetap berada di `assets/js/app.js`.
- Nilai `SUPABASE_ANON_KEY` adalah publishable/anon key; jangan menaruh server key atau API key rahasia di frontend.
- Link referral sekarang dibuat dari URL aplikasi yang sedang dibuka, lalu disalin menggunakan Clipboard API dengan fallback untuk browser yang tidak mendukungnya.
- Tampilan dashboard mengambil pola visual shadcn-admin: sidebar, header ringkas, kartu statistik, panel, tabel, badge, dan mode terang/gelap. Semua fitur Oliv yang ada tetap dipertahankan.