# Konsep Website Portofolio: RadityazDev (v2)

Dokumen ini adalah versi yang disempurnakan dari rancangan awal. Selain struktur halaman dan panduan UI/UX, ditambahkan strategi konten, aksesibilitas, performa, SEO, rekomendasi teknis, dan roadmap pengerjaan agar rancangan siap dieksekusi.

---

## 0. Fondasi Strategi

### 0.1. Tujuan Website
1. **Utama:** Membuat recruiter/klien yakin dalam < 30 detik bahwa Anda kompeten.
2. **Konversi:** Mendorong 3 aksi: *lihat proyek*, *download CV*, *hubungi saya*.
3. **Branding:** Menunjukkan karakter dan cara berpikir, bukan sekadar daftar teknologi.

### 0.2. Target Pengunjung
| Pengunjung | Yang dicari | Yang harus mereka temukan cepat |
|---|---|---|
| Recruiter / HR | Kecocokan skill & pengalaman | Tech stack, proyek unggulan, CV |
| Hiring manager / tech lead | Kualitas kode & cara berpikir | Studi kasus, GitHub, keputusan teknis |
| Klien / freelance | Kemampuan menyelesaikan masalah bisnis | Hasil nyata, testimoni, cara kontak |

### 0.3. Positioning (Nilai Jual)
Tentukan **satu kalimat** yang spesifik. Hindari klaim generik seperti "pekerja keras".
- Formula: *Saya membantu [siapa] membangun [apa] sehingga [hasil].*
- Contoh: "Saya membangun aplikasi web yang cepat dan mudah dirawat, dari desain database sampai antarmuka."

### 0.4. Prinsip Desain
- **Cepat dipindai:** pengunjung men-scroll, bukan membaca.
- **Bukti > klaim:** tampilkan proyek nyata, angka, dan tautan.
- **Konsisten:** satu sistem warna, tipografi, dan spasi di seluruh halaman.
- **Inklusif:** bisa dipakai di HP, keyboard, dan pembaca layar.

---

## 1. Struktur Halaman (Sitemap & Layout)

Ide: *single-page* untuk halaman utama, ditambah halaman detail untuk studi kasus proyek.

```
/                 -> Beranda (Hero, Tentang, Skill, Proyek, Testimoni, Kontak)
/proyek/[slug]    -> Studi kasus per proyek
/blog (opsional)  -> Tulisan teknis
/404              -> Halaman error kustom
```

### 1.1. Header (Navigasi)
- **Logo:** Teks tebal "RadityazDev" atau monogram "RD" di kiri atas.
- **Menu:** Beranda, Tentang, Keahlian, Proyek, Kontak (*anchor link* dengan *smooth scroll*).
- **Indikator aktif:** menu menyala sesuai section yang sedang terlihat (*scrollspy*).
- **CTA:** Tombol "Download CV" di kanan atas.
- **Kontrol tambahan:** *toggle* tema (gelap/terang) dan, opsional, pilihan bahasa ID/EN.
- **Perilaku:** *sticky*, mengecil/berubah transparan saat di-scroll.
- **Mobile:** menu *hamburger* yang membuka panel layar penuh, area sentuh minimal 44×44px.

### 1.2. Hero Section
- **Headline:** Sapaan kuat dan spesifik. Contoh: "Halo, saya Raditya. Saya membangun aplikasi web yang cepat dan rapi."
- **Sub-headline:** 1-2 kalimat tentang nilai jual dan fokus teknologi.
- **Status ketersediaan:** *badge* kecil, misalnya "● Terbuka untuk proyek & lowongan" (hijau). Perbarui secara berkala atau hapus jika tidak relevan.
- **Tombol CTA:** Primary "Lihat Proyek", Secondary "Hubungi Saya".
- **Bukti cepat (opsional):** 3 angka singkat, misalnya "X proyek selesai · Y tahun pengalaman · Z kontribusi open-source". Hanya pakai angka yang benar.
- **Visual:** foto profesional kasual, avatar 3D, atau ilustrasi teknologi. Pilih satu gaya dan konsisten.
- **Indikator scroll:** panah/ikon mouse kecil di bagian bawah.

### 1.3. About Me (Tentang Saya)
- **Deskripsi singkat (maks. 3 paragraf pendek):** latar belakang, passion, pendekatan *problem-solving*.
- **Hal yang membedakan:** satu cerita atau prinsip kerja (mis. "saya selalu mulai dari masalah pengguna").
- **Fakta singkat:** lokasi (Yogyakarta, jika ingin dicantumkan), bahasa, ketersediaan kerja jarak jauh.
- **Timeline:** pengalaman kerja, magang, pendidikan, sertifikasi, atau pencapaian relevan (urut terbaru ke terlama).
- **Sisi personal (opsional):** hobi atau minat singkat agar terasa manusiawi.

### 1.4. Skills & Tech Stack
- **Kategori:** *Front-End*, *Back-End*, *Database*, *DevOps/Tools*, serta *Sedang dipelajari*.
- **Visualisasi:** ikon/logo teknologi tanpa *progress bar* persentase (persentase tidak bermakna dan sulit dipertanggungjawabkan).
- **Penekanan:** tandai 3-5 teknologi andalan (*core stack*) agar tidak terlihat seperti daftar belanja.
- **Aksesibilitas:** setiap ikon punya label teks (bukan hanya gambar).
- **Soft skill:** cukup 3-4 poin singkat yang dibuktikan lewat contoh, bukan klaim.

### 1.5. Portfolio / Projects
- **Tampilan:** *grid* 3-6 proyek unggulan (kualitas > kuantitas), dengan filter kategori jika proyek lebih dari 6.
- **Urutan:** proyek paling kuat dan paling relevan dengan target pekerjaan di posisi pertama.
- **Kartu proyek:**
  - *Screenshot*/*mockup* (rasio konsisten, mis. 16:10, format WebP).
  - Judul dan deskripsi satu kalimat (fokus pada masalah dan hasil).
  - *Tag* tech stack.
  - Peran Anda (solo, tim, atau kontributor).
  - Tautan: "Live Demo", "GitHub Repo", dan "Baca Studi Kasus".
- **Template studi kasus (halaman detail):**
  1. **Ringkasan:** apa proyeknya, untuk siapa.
  2. **Masalah:** tantangan yang ingin diselesaikan.
  3. **Solusi & keputusan teknis:** mengapa memilih teknologi tertentu.
  4. **Tantangan & pembelajaran:** hal sulit dan cara mengatasinya.
  5. **Hasil:** metrik, umpan balik, atau dampak (jika ada).
  6. **Galeri:** screenshot/video singkat.
- **Jika belum punya proyek klien:** gunakan proyek pribadi, tiruan produk nyata dengan perbaikan, atau kontribusi *open-source*, lalu jelaskan konteksnya dengan jujur.
- **README GitHub:** pastikan tiap repo yang ditautkan punya README rapi (deskripsi, cara menjalankan, tangkapan layar).

### 1.6. Testimoni & Validasi Sosial (Baru, opsional)
- 2-3 kutipan singkat dari dosen, rekan tim, atau klien (dengan izin, nama, dan peran).
- Alternatif jika belum ada: rekomendasi LinkedIn, sertifikat, atau pencapaian lomba.

### 1.7. Contact Section
- **Ajakan (copywriting):** "Punya ide atau proyek? Mari wujudkan bersama."
- **Formulir:** Nama, Email, Pesan, tombol "Kirim", ditambah *honeypot* anti-spam atau reCAPTCHA/Turnstile.
- **Status formulir:** *loading*, pesan sukses, pesan error yang jelas, dan validasi inline.
- **Alternatif langsung:** email (tombol salin), WhatsApp, atau tautan jadwal singkat.
- **Ekspektasi respons:** "Biasanya saya membalas dalam 1-2 hari kerja."
- **Tautan sosial:** LinkedIn, GitHub, Email. Tambahkan Dribbble/Behance hanya jika memang berisi karya desain; pertimbangkan X/Twitter atau Dev.to jika aktif menulis.

### 1.8. Footer
- Teks hak cipta (© 2026 RadityazDev).
- Tombol *Back to top*.
- Tautan cepat ke menu utama dan sosial.
- Opsional: "Dibuat dengan [teknologi]" dan tautan ke repo website ini.

---

## 2. Panduan UI/UX (Estetika & Interaksi)

### 2.1. Skema Warna
- **Tema utama:** *Dark mode* modern. Gunakan abu-abu gelap seperti `#121212` atau `#1A1A2E`, hindari hitam pekat `#000000`.
- **Warna aksen:** pilih **satu** aksen utama (neon green, electric blue, atau gradien ungu-merah muda) dan satu aksen pendukung. Terlalu banyak warna membuat tampilan berantakan.
- **Kontras:** teks harus memenuhi rasio WCAG AA (minimal 4,5:1 untuk teks biasa, 3:1 untuk teks besar). Cek dengan alat seperti WebAIM Contrast Checker.
- **Mode terang:** sediakan palet terang yang dirancang sungguh-sungguh (bukan sekadar inversi), simpan pilihan pengguna, dan ikuti `prefers-color-scheme` sebagai default.

**Contoh design token (CSS variables):**

```css
:root {
  --bg: #f7f7fb;
  --surface: #ffffff;
  --text: #14141f;
  --text-muted: #5b5b70;
  --accent: #5b5bf0;
  --border: #e3e3ee;
  --radius: 12px;
}
:root[data-theme="dark"] {
  --bg: #121212;
  --surface: #1a1a2e;
  --text: #ececf4;
  --text-muted: #a0a0b8;
  --accent: #6ee7b7;
  --border: #2a2a42;
}
```

### 2.2. Tipografi
- **Heading:** *font* modern dan *tech-savvy* (Space Grotesk, Syne, atau Poppins).
- **Body:** *sans-serif* yang sangat terbaca (Inter, Roboto, atau Plus Jakarta Sans).
- **Kode/aksen teknis (opsional):** JetBrains Mono atau Fira Code untuk label kecil dan *tag*.
- **Aturan:** maksimal 2 keluarga font (3 bila memakai monospace), skala ukuran konsisten, gunakan `clamp()` agar heading responsif, tinggi baris 1,5-1,7 untuk paragraf, lebar baris sekitar 60-75 karakter.
- **Performa:** muat hanya bobot yang dipakai (mis. 400, 500, 700) dan gunakan `font-display: swap`.

### 2.3. Sistem Spasi & Grid
- Skala spasi kelipatan 4/8px (4, 8, 16, 24, 32, 48, 64, 96).
- Lebar kontainer maksimum sekitar 1200px dengan padding samping yang konsisten.
- Jarak antar-section lega (96-128px di desktop) agar halaman bernapas.

### 2.4. Bentuk dan Elemen UI
- **Sudut membulat:** *border-radius* 8px-12px pada tombol dan kartu (gunakan nilai yang sama secara konsisten).
- **Bento grid:** susun bagian "Tentang" atau "Keahlian" dalam kotak asimetris ala *bento box*. Di mobile ubah menjadi satu kolom.
- **Glassmorphism:** efek semi-transparan dengan *blur* pada navbar atau kartu tertentu. Pakai secukupnya dan pastikan teks tetap kontras. Sediakan *fallback* warna solid untuk peramban yang tidak mendukung `backdrop-filter`.
- **Status interaktif:** setiap elemen punya status *default, hover, focus, active, disabled*.

### 2.5. Animasi & Interaksi (*Micro-interactions*)
- **Hover:** tombol/kartu proyek terangkat sedikit (`translateY(-4px)`) dengan bayangan lembut, durasi 150-250ms.
- **Scroll reveal:** *fade-in-up* ringan saat digulir (Intersection Observer, animasi sekali saja).
- **Typing effect:** efek mesin tik pada headline Hero. Batasi pada 2-4 frasa pendek, pastikan teks lengkap tetap ada untuk pembaca layar, dan jangan menunda tombol CTA.
- **Kursor kustom/parallax (opsional):** hanya bila tidak mengganggu performa.
- **Transisi halaman:** transisi halus antara beranda dan studi kasus.
- **Aksesibilitas gerak:** hormati `prefers-reduced-motion` dengan menonaktifkan atau menyederhanakan animasi.

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

### 2.6. Visual Pelengkap
- Pola abstrak redup, *blob*, atau *mesh gradient* di latar Hero untuk memecah ruang kosong.
- Jaga agar dekorasi tidak bersaing dengan teks (opasitas rendah, tidak di belakang paragraf panjang).
- Gunakan SVG atau gambar yang dioptimasi agar tidak memperberat halaman.

### 2.7. Microcopy & Nada Bahasa
- Gunakan bahasa yang hangat, ringkas, dan percaya diri, tanpa berlebihan.
- Tombol berupa kata kerja jelas: "Lihat Proyek", "Kirim Pesan", "Unduh CV".
- Pesan error membantu: "Email belum valid. Contoh: nama@email.com".
- Putuskan konsisten memakai "saya" (formal-santai) di seluruh halaman.

---

## 3. Aksesibilitas (A11y)

- Struktur HTML semantik: `header`, `nav`, `main`, `section`, `footer`, dan satu `h1`.
- *Skip link* "Lewati ke konten utama".
- Semua gambar punya `alt` bermakna; gambar dekoratif memakai `alt=""`.
- Navigasi penuh dengan keyboard; *focus ring* terlihat jelas (jangan hanya `outline: none`).
- Label formulir terhubung ke input; pesan error diumumkan lewat `aria-live`.
- Jangan mengandalkan warna saja untuk menyampaikan informasi.
- Uji dengan Lighthouse, axe DevTools, dan coba navigasi memakai keyboard.

---

## 4. Responsif & Mobile-First

- Rancang dari layar kecil (360px) lalu perluas: 640 / 768 / 1024 / 1280px.
- Bento grid dan grid proyek menjadi 1 kolom di mobile, 2 kolom di tablet.
- Tombol dan tautan mudah disentuh, teks minimal 16px.
- Pastikan tidak ada *scroll* horizontal di semua ukuran layar.
- Uji di perangkat nyata dan beberapa peramban (Chrome, Safari, Firefox).

---

## 5. Performa & SEO

### 5.1. Target Performa
- Lighthouse **90+** untuk Performance, Accessibility, Best Practices, SEO.
- Core Web Vitals: LCP < 2,5 detik, CLS < 0,1, INP < 200ms.

### 5.2. Teknik
- Gambar WebP/AVIF, ukuran sesuai tampilan, `loading="lazy"` untuk gambar di bawah layar, dan atribut `width`/`height` untuk mencegah pergeseran tata letak.
- Muat font secara efisien; pertimbangkan *self-hosting*.
- Pisahkan kode (*code splitting*), hindari pustaka animasi yang berat bila tidak perlu.
- Pakai CDN/hosting dengan cache yang baik.

### 5.3. SEO Dasar
- Judul dan meta description unik, misalnya: "Raditya | Full-Stack Web Developer di Yogyakarta".
- Open Graph dan Twitter Card (gambar pratinjau 1200×630px) agar tautan tampil menarik saat dibagikan.
- Data terstruktur `Person` (JSON-LD), `sitemap.xml`, `robots.txt`, dan favicon.
- URL bersih dan deskriptif (`/proyek/nama-proyek`).
- Daftarkan situs ke Google Search Console.
- Pertimbangkan domain khusus (mis. `radityazdev.com` atau `.dev`) agar terlihat profesional.

---

## 6. Rekomendasi Teknis (Opsional)

| Kebutuhan | Pilihan |
|---|---|
| Framework | Next.js, Astro (sangat ringan untuk situs statis), atau React + Vite |
| Styling | Tailwind CSS atau CSS Modules |
| Animasi | Framer Motion, GSAP, atau CSS murni |
| Formulir | Formspree, Resend + API route, atau EmailJS |
| Konten | MDX/Markdown untuk studi kasus dan blog |
| Hosting | Vercel, Netlify, atau Cloudflare Pages |
| Analitik | Plausible, Umami, atau Google Analytics (hormati privasi) |
| Kualitas | ESLint, Prettier, Lighthouse CI |

Catatan: karena situs ini sendiri adalah portofolio, **kualitas kode dan struktur repo-nya ikut dinilai**. Jadikan repo publik yang rapi dengan README yang baik.

---

## 7. Strategi Konten & Pemeliharaan

- Perbarui proyek dan CV minimal tiap 3-6 bulan.
- Ganti proyek lama yang lemah dengan karya yang lebih baru.
- Pastikan semua tautan (demo, GitHub, CV) masih aktif.
- Siapkan CV versi PDF yang ringan, namanya jelas (mis. `CV_Raditya_FullStack.pdf`).
- Opsional: blog/catatan teknis untuk menunjukkan kedalaman dan menambah trafik organik.

---

## 8. Roadmap Pengerjaan

| Tahap | Fokus | Hasil |
|---|---|---|
| 1. Riset & konten | Positioning, copywriting, pilih proyek, kumpulkan aset | Naskah dan aset siap |
| 2. Wireframe | Sketsa tata letak desktop dan mobile (Figma) | Wireframe disetujui |
| 3. UI design | Warna, tipografi, komponen, design token | Prototipe visual |
| 4. Pengembangan | Bangun halaman, responsif, animasi | Situs berjalan di lokal |
| 5. Pengujian | A11y, performa, lintas peramban, formulir | Skor Lighthouse tercapai |
| 6. Peluncuran | Domain, SEO, analitik, bagikan | Situs live |
| 7. Iterasi | Kumpulkan masukan, perbarui konten | Peningkatan berkelanjutan |

---

## 9. Checklist Sebelum Rilis

- [ ] Headline Hero spesifik dan jelas dalam 5 detik.
- [ ] 3-6 proyek unggulan dengan demo/GitHub yang aktif.
- [ ] Setiap proyek punya peran, tech stack, dan hasil.
- [ ] CV dapat diunduh dan terbaru.
- [ ] Formulir kontak berfungsi (sudah dites kirim sampai terima).
- [ ] Tampilan nyaman di mobile, tablet, dan desktop.
- [ ] Kontras warna lolos WCAG AA; keyboard bisa mengakses semuanya.
- [ ] `prefers-reduced-motion` dihormati.
- [ ] Meta tag, Open Graph, favicon, sitemap terpasang.
- [ ] Skor Lighthouse 90+ di semua kategori.
- [ ] Tidak ada typo, tautan rusak, atau teks placeholder ("Lorem ipsum").
- [ ] Halaman 404 kustom tersedia.
- [ ] Minta 1-2 orang lain mencoba dan memberi masukan.

---

## 10. Kesalahan Umum yang Perlu Dihindari

- Terlalu banyak proyek berkualitas rendah (lebih baik 3 yang kuat).
- Animasi berlebihan yang memperlambat dan melelahkan pengunjung.
- Menampilkan *progress bar* skill berupa persentase.
- Proyek tanpa penjelasan masalah, peran, dan hasil.
- Tautan demo mati atau repo tanpa README.
- Teks kecil, kontras rendah, atau tampilan rusak di HP.
- Menyembunyikan informasi kontak.
