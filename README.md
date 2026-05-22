# Edu AI - Landing Page Digital Business

Repositori ini berisi kode sumber untuk landing page resmi **Edu AI**—sebuah platform pembelajaran pintar bertenaga AI yang dirancang untuk membantu mahasiswa dan pelajar belajar lebih cepat, merangkum materi secara otomatis, dan menyusun jadwal belajar yang optimal.

Aplikasi ini dibangun menggunakan **Vue.js 3 (Vite)** dan **Bootstrap 5** dengan pendekatan komponen modular (Single File Components) dan arsitektur single-page application bergulir panjang, serta dilengkapi sistem routing untuk kemudahan ekspansi halaman di masa depan.

---

## 🛠️ Tech Stack

- **Core Framework**: Vue 3 (SFC `<script setup>`)
- **Build Tool**: Vite
- **Styling**: Bootstrap 5 & Vanilla CSS (Kustomisasi Variabel Brand)
- **Routing**: Vue Router 4 (Mendukung smooth scrolling anchor)
- **Icons**: Bootstrap Icons

---

## 📂 Struktur Folder Proyek

Proyek ini menggunakan struktur folder terpisah agar setiap section halaman mudah dikelola dan dimodifikasi secara mandiri:

```
src/
├── assets/
│   ├── css/
│   │   └── main.css          # Desain sistem, warna brand violet & kustomisasi Bootstrap
│   └── logo.svg              # Logo utama Edu AI
├── components/
│   ├── Navbar.vue            # Sticky glassmorphism header & navigasi smooth scroll
│   ├── Footer.vue            # Footer berkolom lengkap dengan langganan newsletter
│   └── sections/
│       ├── HeroSection.vue   # Banner utama dengan highlight teks AI, kurva kuning SVG, & mockup dashboard
│       ├── SponsorSection.vue# Baris sponsor / rekanan dengan animasi geser horizontal otomatis (infinite loop)
│       ├── FeaturesSection.vue # Kartu fitur utama (AI Penjelasan, Rangkuman, & Jadwal Rapi)
│       ├── PricingSection.vue  # Tabel harga interaktif dengan switch toggle Bulanan/Tahunan
│       └── ContactSection.vue  # Form hubungi kami dengan validasi loading & informasi sosial media
├── router/
│   └── index.js              # Manajemen rute halaman utama & halaman tambahan
├── views/
│   ├── HomeView.vue          # Halaman utama (Single page scroll aggregator)
│   └── OtherView.vue         # Template rute baru (Pendaftaran akun dummy)
├── App.vue                   # Entry point layout utama
└── main.js                   # Inisialisasi Vue app & impor Bootstrap + CSS kustom
```

---

## ✨ Fitur Landing Page

1. **Desain Premium & Glassmorphism**: Tampilan modern menggunakan kontras warna violet pastel, latar belakang gradien halus, efek *blur* panel navigasi, dan animasi interaktif.
2. **Infinite Marquee Sponsor**: Baris logo mitra kerja sama (Amikom, Notion, Intercom, dll.) yang bergeser mulus secara otomatis. Animasi akan terjeda otomatis saat kursor diarahkan (*hover-to-pause*).
3. **Mockup Dashboard Interaktif**: Mockup aplikasi web dark-theme di kolom Hero yang didesain menggunakan HTML/CSS murni (tanpa gambar statis) sehingga responsif, lengkap dengan widget aktif beranimasi goyang (*Active Users*, *Flag*, *Database*).
4. **Billing Switcher**: Kalkulator harga dinamis pada seksi *Pricing* untuk menghitung harga berlangganan bulanan vs tahunan (diskon 20%).
5. **Interactive Contact Form**: Form kontak interaktif dengan feedback status pengiriman (*loading simulator* & *success overlay state*).
6. **Siap Tambah Halaman**: Konfigurasi router sudah aktif. Tombol *Signup* di navbar akan mengarahkan user ke halaman baru (`/other`) untuk membuktikan sistem multi-page siap digunakan.

---

## 🚀 Cara Menjalankan Project

### Prasyarat
Pastikan Anda sudah menginstal [Node.js](https://nodejs.org/) di komputer Anda.

### Langkah Instalasi

1. Clone repositori ini ke penyimpanan lokal Anda:
   ```bash
   git clone https://github.com/username/Edu-AI-LandingPage.git
   cd Edu-AI-LandingPage
   ```

2. Instal semua dependensi yang diperlukan:
   ```bash
   npm install
   ```

3. Jalankan server pengembangan lokal (local development server):
   ```bash
   npm run dev
   ```
   *Buka browser di alamat `http://localhost:5173/` untuk melihat web.*

4. Untuk membuat versi produksi siap unggah (production build):
   ```bash
   npm run build
   ```
   *Hasil kompilasi file yang optimal akan berada di dalam folder `dist/`.*

---

## 📞 Kontak & Informasi Sosial Media

- **Website Demo**: [https://edu-ai-blond.vercel.app/](https://edu-ai-blond.vercel.app/)
- **Instagram**: [@eduai.id](https://instagram.com/eduai.id)
- **Kantor**: Tech Hub Yogyakarta (Condongcatur, Depok, Sleman, Yogyakarta)
