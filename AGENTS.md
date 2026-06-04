# AGENTS.md — SmartWallet UI Prototype

## Ringkasan Arsitektur

Proyek ini adalah prototipe UI satu halaman (single-file HTML) untuk aplikasi e-wallet FinTech bernama SmartWallet. Tidak ada framework JavaScript atau proses build — seluruh kode berada di `index.html`.

## Struktur File

```
index.html      # Seluruh UI, styling, dan logika interaksi
README.md       # Dokumentasi pengguna
AGENTS.md       # Dokumentasi untuk AI agent (file ini)
```

## Keputusan Arsitektur Penting

- **Single-file approach**: Sengaja dipilih agar prototipe mudah dibagikan dan dijalankan tanpa setup. Tidak ada bundler, tidak ada dependensi lokal.
- **Tailwind via CDN + `tailwind.config`**: Konfigurasi tema (warna `brand`, font, animasi kustom) didefinisikan inline di tag `<script>` sebelum Tailwind dimuat.
- **Animasi CSS murni**: Bar chart dan progress bar menggunakan `@keyframes` CSS dengan `animation-delay` dan variabel CSS `--bar-width` untuk mendukung nilai dinamis per elemen. IntersectionObserver digunakan untuk memulai animasi saat elemen masuk viewport.
- **Toast system**: Diimplementasikan dengan Vanilla JS — fungsi `showToast(type, title, message)` membuat elemen DOM, menambahkan kelas animasi, lalu auto-dismiss setelah 3,2 detik.
- **Avatar**: Menggunakan DiceBear API dengan fallback ke `ui-avatars.com` jika gagal dimuat.

## Konvensi Koding

- Kelas Tailwind digunakan secara konsisten; style inline hanya untuk nilai yang tidak dapat diekspresikan oleh Tailwind (mis. `background: linear-gradient(...)`).
- Warna utama menggunakan alias `brand-*` (peta ke `emerald/teal` gelap) yang didefinisikan di `tailwind.config`.
- Semua teks konten dalam Bahasa Indonesia.
- Interaksi pengguna (klik tombol, ikon nav) selalu memanggil `showToast()` sebagai sistem feedback.

## Cara Mengembangkan

Untuk menambahkan halaman baru (mis. Expense, Profile):
1. Tambahkan section HTML baru di dalam `.scroll-hidden` container
2. Ubah event handler `onclick` di bottom nav untuk toggle visibility antar halaman
3. Gunakan kelas `fade-up-*` untuk animasi masuk yang konsisten
