# Tutorial: Mengedit & Kustomisasi Template Portofolio Putih

### Modul — HTML, CSS, JavaScript

Di tutorial ini, kamu akan mengedit dan mengkustomisasi template website portofolio siap pakai yang ada di folder **`portofolio-putih/`**. Kamu akan mengubah nama, deskripsi, foto profil, riwayat pendidikan, daftar proyek beserta gambarnya, informasi kontak, hingga warna tampilan website sesuai identitas kamu sendiri.

---

## Daftar Isi

1. [Persiapan & Struktur File](#1-persiapan--struktur-file)
2. [Panduan Kustomisasi `portofolio-putih/index.html`](#2-panduan-kustomisasi-portofolio-putihindexhtml)
   - [Langkah 1: Mengubah Judul Tab Browser & Meta](#langkah-1-mengubah-judul-tab-browser--meta)
   - [Langkah 2: Mengubah Nama & Deskripsi Hero/Profil](#langkah-2-mengubah-nama--deskripsi-heroprofil)
   - [Langkah 3: Mengubah Foto Profil](#langkah-3-mengubah-foto-profil)
   - [Langkah 4: Mengubah Riwayat Pendidikan](#langkah-4-mengubah-riwayat-pendidikan)
   - [Langkah 5: Mengubah & Menambah Daftar Proyek](#langkah-5-mengubah--menambah-daftar-proyek)
   - [Langkah 6: Mengubah Gambar Proyek](#langkah-6-mengubah-gambar-proyek)
   - [Langkah 7: Mengubah Informasi Kontak & Footer](#langkah-7-mengubah-informasi-kontak--footer)
   - [Langkah 8: Mengkustomisasi Tema Warna (CSS Variable)](#langkah-8-mengkustomisasi-tema-warna-css-variable)
3. [Cara Menjalankan & Memeriksa Hasil](#3-cara-menjalankan--memeriksa-hasil)

---

## 1. Persiapan & Struktur File

### Download Template

1. Buka website galeri template di: **https://template-portofolio-pkm.vercel.app/**
2. Pilih **Template Terang** (putih), lalu klik tombol download.
3. File yang akan terunduh bernama **`template-portofolio-terang.zip`**.

### Extract File ZIP

1. Temukan file `template-portofolio-terang.zip` di folder **Downloads**.
2. Klik kanan file tersebut, lalu pilih **Extract All...** (Windows) atau **Extract Here**.
3. Tentukan lokasi tujuan extract, misalnya di folder `Dokumen` atau `Desktop`.
4. Klik **Extract**. Setelah selesai, akan muncul folder bernama **`portofolio-putih/`**.

### Struktur Folder Hasil Extract

```
portofolio-putih/
  ├── index.html        <-- File HTML utama yang akan kita edit
  └── img/
      ├── profile.jpg   <-- Foto profil placeholder
      ├── proyek1.jpeg  <-- Gambar proyek 1 placeholder
      ├── proyek2.jpeg  <-- Gambar proyek 2 placeholder
      └── proyek3.jpeg  <-- Gambar proyek 3 placeholder
```

> **Persiapan sebelum mulai mengedit:**
> 1. Siapkan **foto profil kamu** (format `.jpg` atau `.png`).
> 2. Siapkan **gambar untuk setiap proyek** kamu (format `.jpg`, `.jpeg`, atau `.png`).
> 3. Simpan semua gambar tersebut ke dalam folder `portofolio-putih/img/`.

---

## 2. Panduan Kustomisasi `portofolio-putih/index.html`

Buka file **`portofolio-putih/index.html`** di Text Editor (misalnya VS Code), lalu ikuti petunjuk langkah demi langkah di bawah ini:

---

### Langkah 1: Mengubah Judul Tab Browser & Meta

#### Letak Kode (Baris 6 & 11):
```html
<title>Portofolio - Nama Anda</title>
...
<meta property="og:title" content="Portofolio - Nama Anda" />
```

#### Perubahan (Ganti dengan nama kamu):
```html
<title>Portofolio - Budi Santoso</title>
...
<meta property="og:title" content="Portofolio - Budi Santoso" />
```

---

### Langkah 2: Mengubah Nama & Deskripsi Hero/Profil

#### Letak Kode (Baris 562 - 568):
Cari tag `<section id="profil" class="hero">`:

```html
<p class="greeting">Halo, saya</p>
<h1>Nama Anda</h1>
<p>
   Seorang pengembang, desainer, atau profesional kreatif
   yang suka membangun produk digital yang bermanfaat dan
   menyenangkan untuk digunakan.
</p>
```

#### Perubahan (Sesuaikan dengan identitasmu):
```html
<p class="greeting">Halo, saya</p>
<h1>Budi Santoso</h1>
<p>
   Siswa SMAN 10 TAMSEL yang menyukai dunia pemrograman web, desain grafis, dan pembuatan aplikasi digital sederhana.
</p>
```

---

### Langkah 3: Mengubah Foto Profil

#### Letak Kode (Baris 578 - 585):
Cari tag `<div class="hero-image">`:

```html
<div class="hero-image">
   <img
      src="img/profile.jpg"
      alt="Foto profil Nama Anda"
      width="400"
      height="400"
   />
</div>
```

#### Perubahan:
Ganti `img/profile.jpg` dengan nama file fotomu yang sudah disalin ke folder `portofolio-putih/img/`:

```html
<div class="hero-image">
   <img
      src="img/foto-saya.jpg"
      alt="Foto profil Budi Santoso"
      width="400"
      height="400"
   />
</div>
```

---

### Langkah 4: Mengubah Riwayat Pendidikan

#### Letak Kode (Baris 597 - 619):
Cari bagian `<section id="pendidikan" class="section education">`. Di dalamnya terdapat beberapa elemen `<article class="timeline-item">`:

```html
<article class="timeline-item">
   <div class="timeline-header">
      <h3>Sarjana Teknik Informatika</h3>
      <span class="year">2018 — 2022</span>
   </div>
   <p class="institution">Universitas Contoh Indonesia</p>
</article>
```

#### Perubahan (Sesuaikan dengan riwayat sekolahmu):
```html
<article class="timeline-item">
   <div class="timeline-header">
      <h3>SMAN 10 Tambun Selatan</h3>
      <span class="year">2024 — Sekarang</span>
   </div>
   <p class="institution">Kelas 11 IPA / IPS</p>
</article>
<article class="timeline-item">
   <div class="timeline-header">
      <h3>SMP Negeri 1 Tambun Selatan</h3>
      <span class="year">2021 — 2024</span>
   </div>
   <p class="institution">Lulusan SMP</p>
</article>
```

---

### Langkah 5: Mengubah & Menambah Daftar Proyek

#### Letak Kode (Baris 631 - 684):
Cari bagian `<section id="proyek" class="section">`. Setiap proyek dibungkus oleh elemen `<article class="project-card">`:

```html
<article class="project-card">
   <img
      src="img/proyek1.jpeg"
      alt="Tampilan aplikasi dashboard analitik"
   />
   <div class="project-body">
      <h3>Dashboard Analitik</h3>
      <p>
         Dashboard interaktif untuk memantau metrik bisnis
         secara real-time.
      </p>
      <div class="tags">
         <span class="tag">React</span>
         <span class="tag">Tailwind</span>
         <span class="tag">Chart.js</span>
      </div>
   </div>
</article>
```

#### Perubahan (Edit teks judul, deskripsi, dan tag teknologi):
```html
<article class="project-card">
   <img
      src="img/proyek1.jpeg"
      alt="Aplikasi Kalkulator HTML"
   />
   <div class="project-body">
      <h3>Kalkulator Sederhana</h3>
      <p>
         Aplikasi kalkulator interaktif untuk operasi matematika dasar dengan JavaScript.
      </p>
      <div class="tags">
         <span class="tag">HTML</span>
         <span class="tag">CSS</span>
         <span class="tag">JavaScript</span>
      </div>
   </div>
</article>
```

#### Cara Menambah Proyek Baru:
Duplikat satu blok `<article class="project-card">...</article>` lalu paste tepat di bawah proyek sebelumnya (sebelum `</div>` penutup `project-grid`).

---

### Langkah 6: Mengubah Gambar Proyek

Template sudah menyediakan 3 file gambar placeholder di folder `portofolio-putih/img/`:
- `proyek1.jpeg` — dipakai oleh kartu proyek pertama
- `proyek2.jpeg` — dipakai oleh kartu proyek kedua
- `proyek3.jpeg` — dipakai oleh kartu proyek ketiga

#### Cara menggantinya:

**Metode 1 — Timpa file lama (paling mudah):**
1. Siapkan gambar proyekmu (misalnya screenshot website atau foto hasil kerja).
2. Ubah nama file gambar tersebut menjadi `proyek1.jpeg` (atau `proyek2.jpeg` / `proyek3.jpeg`).
3. Salin file tersebut ke folder `portofolio-putih/img/`, lalu pilih **Replace** / **Timpa** jika diminta konfirmasi.
4. Buka browser dan refresh halaman — gambar baru akan langsung muncul tanpa perlu mengubah kode HTML.

**Metode 2 — Simpan dengan nama baru lalu ubah kode:**
1. Salin gambar proyekmu ke folder `portofolio-putih/img/` dengan nama berbeda, misalnya `kalkulator.png`.
2. Di dalam `index.html`, cari baris berikut (Baris 632 - 634):
   ```html
   <img
      src="img/proyek1.jpeg"
      alt="Tampilan aplikasi dashboard analitik"
   />
   ```
3. Ganti nilai `src` dan `alt` sesuai nama file dan deskripsi proyekmu:
   ```html
   <img
      src="img/kalkulator.png"
      alt="Tampilan Kalkulator Sederhana"
   />
   ```
4. Lakukan hal yang sama untuk proyek kedua (Baris 650 - 652) dan ketiga (Baris 668 - 670).

> **Catatan:** Pastikan nama file tidak mengandung spasi. Gunakan tanda hubung (`-`) atau garis bawah (`_`) sebagai pengganti spasi. Contoh: `proyek-kalkulator.jpg` bukan `proyek kalkulator.jpg`.

---

### Langkah 7: Mengubah Informasi Kontak & Footer

#### Letak Kode:

1. **Email (Baris 717):**
```html
<a href="mailto:email@anda.com">email@anda.com</a>
```
Ganti dengan email kamu:
```html
<a href="mailto:budi@email.com">budi@email.com</a>
```

2. **No Telepon / WA (Baris 734):**
```html
<a href="tel:+6281234567890">+62 812-3456-7890</a>
```
Ganti dengan nomor WA kamu:
```html
<a href="tel:+6289876543210">+62 898-7654-3210</a>
```

3. **Lokasi (Baris 752):**
```html
<span>Jakarta, Indonesia</span>
```
Ganti dengan kota/domisili kamu:
```html
<span>Bekasi, Indonesia</span>
```

4. **Teks Hak Cipta Footer (Baris 803 - 805):**
```html
<p>
   &copy; 2026 Nama Anda. Dibuat dengan HTML, CSS, dan JavaScript.
</p>
```
Ganti dengan namamu:
```html
<p>
   &copy; 2026 Budi Santoso. Dibuat dengan HTML, CSS, dan JavaScript.
</p>
```

---

### Langkah 8: Mengkustomisasi Tema Warna (CSS Variable)

Website ini menggunakan **CSS Variables** di bagian atas style. Kamu bisa dengan mudah mengubah seluruh skema warna website hanya dengan mengganti beberapa kode warna di dalam `:root`!

#### Letak Kode (Baris 25 - 34):
Cari bagian `<style>` di dalam `<head>`:

```css
:root {
   --bg: #f5f3ee;       /* Warna latar belakang utama */
   --surface: #e8e4dd;  /* Warna kartu & section */
   --text: #2d2d2d;     /* Warna teks paragraf */
   --heading: #0d0d0d;  /* Warna judul & tombol utama */
   --muted: #6b6b6b;    /* Warna teks sekunder / subjudul */
   --border: #d9d4cb;   /* Warna garis tepi / border */
   --radius: 1rem;      /* Kelengkungan sudut kartu */
   --shadow: 0 8px 30px rgba(13, 13, 13, 0.06); /* Bayangan kartu */
}
```

#### Contoh Mengubah ke Tema Modern Blue:
```css
:root {
   --bg: #f0f4f8;       /* Latar biru lembut */
   --surface: #ffffff;  /* Kartu warna putih bersih */
   --text: #334e68;     /* Teks warna biru gelap */
   --heading: #102a43;  /* Judul warna navy */
   --muted: #627d98;    /* Teks sekunder */
   --border: #d9e2ec;   /* Border lembut */
   --radius: 1rem;
   --shadow: 0 8px 30px rgba(16, 42, 67, 0.08);
}
```

---

## 3. Cara Menjalankan & Memeriksa Hasil

1. Simpan file `portofolio-putih/index.html` yang sudah kamu edit (`Ctrl + S`).
2. Buka folder `portofolio-putih/` di File Explorer, lalu **double-click** file `index.html` untuk membukanya di browser (Chrome / Edge / Firefox).
3. Atau di VS Code, klik kanan file `portofolio-putih/index.html` lalu pilih **Open with Live Server** / **Show Preview**.
4. Cek seluruh perubahan:
   - Nama dan foto profil sudah sesuai.
   - Menu navigasi atas saat diklik menggulung secara halus (*smooth scroll*) ke bagian yang dituju.
   - Gambar proyek sudah tampil dengan benar.
   - Informasi pendidikan, proyek, kontak, dan footer sudah diperbarui.
   - Tema warna sesuai dengan selera kamu!

