# SmartWallet — Prototipe UI E-Wallet FinTech

Prototipe antarmuka pengguna (UI) untuk aplikasi dompet digital **SmartWallet**, dibangun sebagai satu file HTML mandiri dengan pendekatan Mobile-First.

## Teknologi

- **Tailwind CSS** (via CDN) — sistem desain utility-first
- **Font Awesome 6** (via CDN) — ikon-ikon UI profesional
- **Google Fonts: DM Sans & DM Serif Display** — tipografi modern dan elegan
- **Vanilla JavaScript** — interaksi dan notifikasi toast tanpa dependensi tambahan

## Cara Menjalankan

Cukup buka file `index.html` di browser modern mana pun — tidak diperlukan proses build atau server lokal.

```bash
open index.html
# atau drag & drop ke browser
```

## Fitur yang Diimplementasikan

- **Header & Profil** dengan avatar, salam personalisasi, dan indikator notifikasi
- **Card Saldo Utama** bergradasi dengan tombol Top-Up & Transfer (efek animasi)
- **Pintasan Menu Cepat** (Bayar, Tagihan, Pulsa, Lainnya)
- **Expense Tracker** dengan visualisasi bar chart per kategori (animasi CSS murni)
- **Virtual Savings** dengan progress bar target tabungan
- **Riwayat Transaksi** dengan ikon kategori dan kode warna
- **Bottom Navigation Bar** (5 menu: Expense, Split Bill, Home, Savings, Profile)
- **Toast Notification** responsif untuk setiap interaksi tombol
- Fitur sembunyikan/tampilkan saldo dengan ketukan
