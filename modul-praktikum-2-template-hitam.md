# Tutorial: Mengedit & Kustomisasi Template Portofolio Hitam

### Modul — HTML, CSS, JavaScript

Di tutorial ini, kamu akan mengedit dan mengkustomisasi template website portofolio siap pakai yang ada di folder **`portofolio-hitam/`**. Kamu akan mengubah nama, deskripsi, foto profil, riwayat pendidikan, daftar proyek beserta gambarnya, daftar prestasi, pengalaman organisasi, informasi kontak, hingga warna tampilan website sesuai identitas kamu sendiri.

---

## Daftar Isi

1. [Persiapan & Struktur File](#1-persiapan--struktur-file)
2. [Panduan Kustomisasi `portofolio-hitam/index.html`](#2-panduan-kustomisasi-portofolio-hitamindexhtml)
   - [Langkah 1: Mengubah Judul Tab Browser & Meta](#langkah-1-mengubah-judul-tab-browser--meta)
   - [Langkah 2: Mengubah Nama & Deskripsi Hero/Profil](#langkah-2-mengubah-nama--deskripsi-heroprofil)
   - [Langkah 3: Mengubah Foto Profil](#langkah-3-mengubah-foto-profil)
   - [Langkah 4: Mengubah Riwayat Pendidikan](#langkah-4-mengubah-riwayat-pendidikan)
   - [Langkah 5: Mengubah & Menambah Daftar Proyek](#langkah-5-mengubah--menambah-daftar-proyek)
   - [Langkah 6: Mengubah Gambar Proyek](#langkah-6-mengubah-gambar-proyek)
   - [Langkah 7: Mengubah Daftar Prestasi](#langkah-7-mengubah-daftar-prestasi)
   - [Langkah 8: Mengubah Daftar Organisasi](#langkah-8-mengubah-daftar-organisasi)
   - [Langkah 9: Mengubah Informasi Kontak & Footer](#langkah-9-mengubah-informasi-kontak--footer)
   - [Langkah 10: Mengkustomisasi Tema Warna (CSS Variable)](#langkah-10-mengkustomisasi-tema-warna-css-variable)
3. [Cara Menjalankan & Memeriksa Hasil](#3-cara-menjalankan--memeriksa-hasil)

---

## 1. Persiapan & Struktur File

### Download Template

1. Buka website galeri template di: **https://template-portofolio-pkm.vercel.app/**
2. Pilih **Template Gelap** (hitam), lalu klik tombol download.
3. File yang akan terunduh bernama **`template-portofolio-gelap.zip`**.

![](gambar/extract-hitam.png)

### Extract File ZIP

1. Temukan file `template-portofolio-gelap.zip` di folder **Downloads**.
2. Klik kanan file tersebut, lalu pilih **Extract All...** (Windows) atau **Extract Here**.
3. Tentukan lokasi tujuan extract, misalnya di folder `Dokumen` atau `Desktop`.
4. Klik **Extract**. Setelah selesai, akan muncul folder bernama **`portofolio-hitam/`**.

### Struktur Folder Hasil Extract

```
portofolio-hitam/
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
> 3. Simpan semua gambar tersebut ke dalam folder `portofolio-hitam/img/`.

---

## 2. Panduan Kustomisasi `portofolio-hitam/index.html`

Buka file **`portofolio-hitam/index.html`** di Text Editor (misalnya VS Code), lalu ikuti petunjuk langkah demi langkah di bawah ini:

---

### Langkah 1: Mengubah Judul Tab Browser & Meta

#### Letak Kode (Baris 6 & 11):
```html
<title>Portofolio — Nama Anda</title>
...
<meta property="og:title" content="Portofolio — Nama Anda" />
```

#### Perubahan (Ganti dengan nama kamu):
```html
<title>Portofolio — Budi Santoso</title>
...
<meta property="og:title" content="Portofolio — Budi Santoso" />
```

#### Hasil:
![](gambar/ganti-title.png)
---

### Langkah 2: Mengubah Nama & Deskripsi Hero/Profil

#### Letak Kode (Baris 697 - 703):
Cari tag `<section id="profil" class="hero">`:

```html
<p class="greeting">Halo, saya</p>
<h1>Nama <em>Anda</em></h1>
<p>
   Seorang pengembang, desainer, atau profesional kreatif
   yang suka membangun produk digital yang bermanfaat dan
   menyenangkan untuk digunakan.
</p>
```

#### Perubahan (Sesuaikan dengan identitasmu):
```html
<p class="greeting">Halo, saya</p>
<h1>Budi <em>Santoso</em></h1>
<p>
   Siswa SMAN 2 Tambun Selatan yang menyukai dunia pemrograman web, desain grafis, dan pembuatan aplikasi digital sederhana.
</p>
```

#### Hasil:
![](gambar/nama-deskripsi-hitam.png)

> **Catatan:** Template hitam menggunakan tag `<em>` untuk memberi aksen warna oranye pada sebagian nama. Sesuaikan mana kata yang ingin kamu tonjolkan.

---

### Langkah 3: Mengubah Foto Profil

#### Letak Kode (Baris 713 - 720):
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
Ganti `img/profile.jpg` dengan nama file fotomu yang sudah disalin ke folder `portofolio-hitam/img/`:

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

#### Letak Kode (Baris 732 - 761):
Cari bagian `<section id="pendidikan" class="section">`. Di template hitam, setiap entri pendidikan dibungkus oleh elemen `<article class="card">`:

```html
<article class="card">
   <div class="card-body">
      <div class="timeline-header">
         <h3>Sarjana Teknik Informatika</h3>
         <span class="year">2018 — 2022</span>
      </div>
      <p class="institution">Universitas Contoh Indonesia</p>
   </div>
</article>
```

#### Perubahan (Sesuaikan dengan riwayat sekolahmu):
```html
<article class="card">
   <div class="card-body">
      <div class="timeline-header">
         <h3>SMAN 2 Tambun Selatan</h3>
         <span class="year">2024 — Sekarang</span>
      </div>
      <p class="institution">Kelas 11 IPA / IPS</p>
   </div>
</article>
<article class="card">
   <div class="card-body">
      <div class="timeline-header">
         <h3>SMP Negeri 1 Tambun Selatan</h3>
         <span class="year">2021 — 2024</span>
      </div>
      <p class="institution">Lulusan SMP</p>
   </div>
</article>
```

#### Hasil:
![](gambar/jenjang-hitam.png)

---

### Langkah 5: Mengubah & Menambah Daftar Proyek

#### Letak Kode (Baris 772 - 827):
Cari bagian `<section id="proyek" class="section">`. Di template hitam, setiap proyek dibungkus oleh elemen `<article class="card project-card">`:

```html
<article class="card project-card">
   <img
      src="img/proyek1.jpeg"
      alt="Tampilan aplikasi dashboard analitik"
   />
   <div class="card-body project-body">
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
<article class="card project-card">
   <img
      src="img/proyek1.jpeg"
      alt="Aplikasi Kalkulator HTML"
   />
   <div class="card-body project-body">
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
Duplikat satu blok `<article class="card project-card">...</article>` lalu paste tepat di bawah proyek sebelumnya (sebelum `</div>` penutup `card-grid`).

#### Hasil:
![](gambar/proyek-hitam.png)

---

### Langkah 6: Mengubah Gambar Proyek

Template sudah menyediakan 3 file gambar placeholder di folder `portofolio-hitam/img/`:
- `proyek1.jpeg` — dipakai oleh kartu proyek pertama
- `proyek2.jpeg` — dipakai oleh kartu proyek kedua
- `proyek3.jpeg` — dipakai oleh kartu proyek ketiga

#### Cara menggantinya:

**Metode 1 — Timpa file lama (paling mudah):**
1. Siapkan gambar proyekmu (misalnya screenshot website atau foto hasil kerja).
2. Ubah nama file gambar tersebut menjadi `proyek1.jpeg` (atau `proyek2.jpeg` / `proyek3.jpeg`).
3. Salin file tersebut ke folder `portofolio-hitam/img/`, lalu pilih **Replace** / **Timpa** jika diminta konfirmasi.
4. Buka browser dan refresh halaman — gambar baru akan langsung muncul tanpa perlu mengubah kode HTML.

**Metode 2 — Simpan dengan nama baru lalu ubah kode:**
1. Salin gambar proyekmu ke folder `portofolio-hitam/img/` dengan nama berbeda, misalnya `kalkulator.png`.
2. Di dalam `index.html`, cari baris berikut (Baris 774 - 776):
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
4. Lakukan hal yang sama untuk proyek kedua (Baris 792 - 794) dan ketiga (Baris 810 - 812).

> **Catatan:** Pastikan nama file tidak mengandung spasi. Gunakan tanda hubung (`-`) atau garis bawah (`_`) sebagai pengganti spasi. Contoh: `proyek-kalkulator.jpg` bukan `proyek kalkulator.jpg`.

---

### Langkah 7: Mengubah Daftar Prestasi

Template hitam memiliki section **Prestasi** dengan tampilan kartu grid (*prestasi-card*). Setiap prestasi ditampilkan dengan nomor urut di tengah kartu, judul, keterangan, dan tahun.

#### Letak Kode (Baris 839 - 872):
Cari bagian `<section id="prestasi" class="section">`. Setiap entri prestasi dibungkus oleh elemen `<div class="prestasi-card">`:

```html
<div class="prestasi-card">
   <span class="prestasi-num">01</span>
   <div class="prestasi-content">
      <h3>Juara 1 Olimpiade Sains Nasional</h3>
      <p>Bidang Informatika &mdash; Tingkat Provinsi</p>
      <span class="year">2023</span>
   </div>
</div>
```

#### Perubahan (Sesuaikan dengan prestasi kamu):
```html
<div class="prestasi-card">
   <span class="prestasi-num">01</span>
   <div class="prestasi-content">
      <h3>Juara 1 Lomba Web Design Tingkat Kota</h3>
      <p>Kategori SMA &mdash; Diselenggarakan oleh Dinas Pendidikan</p>
      <span class="year">2025</span>
   </div>
</div>
<div class="prestasi-card">
   <span class="prestasi-num">02</span>
   <div class="prestasi-content">
      <h3>Peserta OSN Bidang Informatika</h3>
      <p>Seleksi Tingkat Kabupaten Bekasi</p>
      <span class="year">2024</span>
   </div>
</div>
```

#### Cara Menambah Prestasi Baru:
Duplikat satu blok `<div class="prestasi-card">...</div>` lalu paste di bawah prestasi sebelumnya (sebelum `</div>` penutup `prestasi-grid`). Jangan lupa ubah nomor urut pada `<span class="prestasi-num">` (misalnya `03`, `04`, dst.).

#### Hasil:
![](gambar/prestasi-hitam.png)

---

### Langkah 8: Mengubah Daftar Organisasi

Template hitam memiliki section **Organisasi** yang menampilkan daftar pengalaman berorganisasi dalam format kartu dengan nama organisasi, jabatan, tempat, dan periode.

#### Letak Kode (Baris 876 - 909):
Cari bagian `<section id="organisasi" class="section">`. Setiap entri organisasi dibungkus oleh elemen `<div class="org-item">`:

```html
<div class="org-item">
   <div class="org-meta">
      <h3>Himpunan Mahasiswa Teknik Informatika</h3>
      <p class="org-role">Ketua Umum</p>
      <p class="org-place">Universitas Contoh Indonesia</p>
   </div>
   <span class="year">2021 &mdash; 2022</span>
</div>
```

#### Perubahan (Sesuaikan dengan pengalaman organisasimu):
```html
<div class="org-item">
   <div class="org-meta">
      <h3>OSIS SMAN 2 Tambun Selatan</h3>
      <p class="org-role">Anggota Divisi Seni & Budaya</p>
      <p class="org-place">SMAN 2 Tambun Selatan</p>
   </div>
   <span class="year">2024 &mdash; Sekarang</span>
</div>
<div class="org-item">
   <div class="org-meta">
      <h3>Pramuka Gugus Depan 01</h3>
      <p class="org-role">Ketua Regu Putera</p>
      <p class="org-place">SMP Negeri 1 Tambun Selatan</p>
   </div>
   <span class="year">2022 &mdash; 2024</span>
</div>
```

#### Cara Menambah Organisasi Baru:
Duplikat satu blok `<div class="org-item">...</div>` lalu paste di bawah organisasi sebelumnya (sebelum `</div>` penutup `org-grid`).

#### Hasil:
![](gambar/organisasi-hitam.png)

---

### Langkah 9: Mengubah Informasi Kontak & Footer

#### Letak Kode:

1. **Email (Baris 948):**
```html
<a href="mailto:email@anda.com">email@anda.com</a>
```
Ganti dengan email kamu:
```html
<a href="mailto:budi@email.com">budi@email.com</a>
```

2. **No Telepon / WA (Baris 967):**
```html
<a href="tel:+6281234567890">+62 812-3456-7890</a>
```
Ganti dengan nomor WA kamu:
```html
<a href="tel:+6289876543210">+62 898-7654-3210</a>
```

3. **Lokasi (Baris 987):**
```html
<span>Jakarta, Indonesia</span>
```
Ganti dengan kota/domisili kamu:
```html
<span>Bekasi, Indonesia</span>
```

4. **Teks Hak Cipta Footer (Baris 1038 - 1041):**
```html
<p>
   &copy; 2026 Nama Anda. Dibuat dengan HTML, CSS, dan JavaScript
   murni.
</p>
```
Ganti dengan namamu:
```html
<p>
   &copy; 2026 Budi Santoso. Dibuat dengan HTML, CSS, dan JavaScript
   murni.
</p>
```

#### Hasil:
![](gambar/kontak-hitam.png)

---

### Langkah 10: Mengkustomisasi Tema Warna (CSS Variable)

Website ini menggunakan **CSS Variables** di bagian atas style. Template hitam memiliki variabel tambahan untuk warna aksen oranye dan berbagai tingkat gelap permukaan.

#### Letak Kode (Baris 25 - 37):
Cari bagian `<style>` di dalam `<head>`:

```css
:root {
   --bg: #1a1a1a;                /* Warna latar belakang utama */
   --surface: #2d2d2d;           /* Warna kartu & section */
   --surface-elevated: #333333;  /* Permukaan sedikit lebih terang */
   --text: #b0b0b0;              /* Warna teks paragraf */
   --heading: #f5f5f5;           /* Warna judul */
   --muted: #7a7a7a;             /* Warna teks sekunder */
   --accent: #e85d3a;            /* Warna aksen (tombol & highlight) */
   --accent-hover: #ff7043;      /* Warna aksen saat dihover */
   --border: #3a3a3a;            /* Warna garis tepi / border */
   --radius: 1.25rem;            /* Kelengkungan sudut kartu */
   --shadow: 0 12px 40px rgba(0, 0, 0, 0.35); /* Bayangan kartu */
}
```

#### Contoh Mengubah ke Tema Dark Blue:
```css
:root {
   --bg: #0d1117;                /* Latar hitam biru GitHub */
   --surface: #161b22;           /* Kartu gelap */
   --surface-elevated: #21262d;  /* Permukaan sedikit lebih terang */
   --text: #8b949e;              /* Teks abu biru */
   --heading: #e6edf3;           /* Judul putih kebiruan */
   --muted: #6e7681;             /* Teks sekunder */
   --accent: #58a6ff;            /* Aksen biru cerah */
   --accent-hover: #79c0ff;      /* Aksen biru saat hover */
   --border: #30363d;            /* Border abu gelap */
   --radius: 1.25rem;
   --shadow: 0 12px 40px rgba(0, 0, 0, 0.5);
}
```

#### Hasil:
![](gambar/css-hitam.png)

---

## 3. Cara Menjalankan & Memeriksa Hasil

1. Simpan file `portofolio-hitam/index.html` yang sudah kamu edit (`Ctrl + S`).
2. Buka folder `portofolio-hitam/` di File Explorer, lalu **double-click** file `index.html` untuk membukanya di browser (Chrome / Edge / Firefox).
3. Atau di VS Code, klik kanan file `portofolio-hitam/index.html` lalu pilih **Open with Live Server** / **Show Preview**.
4. Cek seluruh perubahan:
   - Nama dan foto profil sudah sesuai.
   - Menu navigasi atas saat diklik menggulung secara halus (*smooth scroll*) ke bagian yang dituju.
   - Gambar proyek sudah tampil dengan benar.
   - Informasi pendidikan, proyek, prestasi, organisasi, kontak, dan footer sudah diperbarui.
   - Tema warna sesuai dengan selera kamu!
