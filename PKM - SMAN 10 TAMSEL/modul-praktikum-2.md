# Tutorial: Membuat Portofolio Sederhana

### Untuk Pemula — HTML, CSS, JavaScript

Di tutorial ini, kita akan membuat **1 file HTML**:

1. `portofolio.html` — halaman portofolio sederhana dengan profil, proyek, pendidikan, dan kontak

File ini berdiri sendiri, jadi tidak perlu file CSS atau JS terpisah. Semua kode (HTML, CSS, JS) ditulis dalam satu file yang sama.

---

## Daftar Isi

1. [Persiapan](#1-persiapan)
2. [File — portofolio.html](#2-file--portofoliohtml)
3. [Cara Menjalankan](#3-cara-menjalankan)

---

## 1. Persiapan

Yang kamu butuhkan:

- **Text editor**, misalnya Notepad, VS Code, atau Sublime Text.
- **Browser**, misalnya Chrome atau Firefox, untuk membuka hasilnya.

Buat 1 folder baru, misalnya folder bernama `belajar-html`. Nanti file akan disimpan di dalam folder itu:

```
belajar-html/
└── portofolio.html
```

---

## 2. File — portofolio.html

Buat file baru bernama `portofolio.html`, lalu ketik (atau salin) kode berikut.

### Langkah 1: Kerangka HTML

Semua file HTML dimulai dengan kerangka dasar ini:

```html
<html>
   <head>
      <title>Portofolio Sederhana</title>
      <style></style>
   </head>
   <body></body>
</html>
```

> `<style>` di dalam `<head>` adalah tempat kita menulis CSS (pengaturan tampilan). `<body>` adalah tempat konten yang terlihat di halaman.

Kalau file ini dibuka di browser sekarang, halamannya masih **kosong putih polos** — karena `<body>` belum diisi apa-apa. Itu wajar, lanjut ke langkah berikutnya.

### Langkah 2: Tambahkan Konten Portofolio

Di dalam `<body>`, tambahkan judul, foto profil, deskripsi singkat, daftar proyek, pendidikan, dan bagian kontak:

```html
<h1>Hai, saya Andi</h1>
<p class="intro">
   Saya membuat desain web sederhana, proyek kreatif, dan solusi digital untuk
   sekolah.
</p>

<div class="profil">
   <img src="gambar/profil.png" alt="Foto Profil" />
   <div>
      <h2>Profil Singkat</h2>
      <p>
         Saya pelajar SMAN 10 yang suka membuat website sederhana dengan HTML,
         CSS, dan JavaScript.
      </p>
   </div>
</div>

<section class="proyek">
   <h2>Proyek Unggulan</h2>
   <div class="card">
      <h3>Website Sekolah</h3>
      <p>
         Desain halaman utama sekolah dengan menu, gambar, dan informasi profil
         singkat.
      </p>
   </div>
   <div class="card">
      <h3>Poster Digital</h3>
      <p>
         Membuat poster acara sekolah menggunakan warna, teks, dan ikon
         sederhana.
      </p>
   </div>
</section>

<section class="pendidikan">
   <h2>Pendidikan</h2>
   <ul>
      <li>SMAN 10 TAMSEL — Kelas 11 IPA</li>
      <li>Pelatihan HTML & CSS</li>
   </ul>
</section>

<section class="kontak">
   <h2>Kontak</h2>
   <p>Klik tombol untuk melihat email dan telepon saya:</p>
   <button onclick="tampilkanKontak()">Tampilkan Kontak</button>
   <p id="infoKontak">-</p>
</section>
```

**Penjelasan:**

- `<h1>` dan `<p>` menampilkan judul dan deskripsi utama.
- `<div class="profil">` berisi foto dan teks profil.
- `<section>` digunakan untuk mengelompokkan proyek, pendidikan, dan kontak agar halaman lebih teratur.
- `button onclick="tampilkanKontak()"` akan menjalankan fungsi JavaScript untuk menampilkan detail kontak.

**Hasil ketika dijalankan:**

Halaman sudah menampilkan judul, deskripsi, profil, daftar proyek, pendidikan, dan tombol kontak. Namun tampilannya masih sederhana karena CSS belum ditambahkan.

### Langkah 3: Tambahkan CSS Sederhana

Sekarang isi bagian `<style>` supaya tampilan portofolio lebih rapi:

```css
body {
   font-family: Arial, sans-serif;
   padding: 20px;
   background-color: #f7f7f7;
}

h1 {
   color: #333333;
}

.intro {
   max-width: 600px;
   line-height: 1.6;
}

.profil {
   display: flex;
   gap: 20px;
   align-items: center;
   margin-top: 20px;
}

.profil img {
   width: 120px;
   border-radius: 10px;
   border: 2px solid #cccccc;
}

.proyek,
.pendidikan,
.kontak {
   margin-top: 30px;
}

.card {
   background-color: white;
   border: 1px solid #dddddd;
   padding: 15px;
   border-radius: 8px;
   margin-top: 10px;
}

ul {
   list-style-type: disc;
   margin-left: 20px;
}

button {
   background-color: #007bff;
   color: white;
   border: none;
   padding: 10px 15px;
   border-radius: 6px;
   cursor: pointer;
}

button:hover {
   background-color: #0056b3;
}

#infoKontak {
   margin-top: 10px;
   font-weight: bold;
}
```

**Penjelasan:**

- `body` mengatur font, jarak, dan latar belakang halaman.
- `.profil` membuat foto dan teks berada dalam baris yang rapi.
- `.card` membuat setiap proyek terlihat seperti kartu putih tersusun rapi.
- `button` memberi warna dan gaya tombol kontak.

**Hasil ketika dijalankan:**

Halaman sekarang terlihat lebih rapi: teks terbaca, proyek terpisah di dalam kartu, dan tombol kontak punya gaya yang jelas. Tapi tombol kontak belum berfungsi, karena JavaScript belum ditambahkan.

### Langkah 4: Tambahkan JavaScript

Terakhir, tambahkan `<script>` sebelum tag penutup `</body>`:

```html
<script>
   function tampilkanKontak() {
      const info = document.getElementById("infoKontak");
      info.textContent = "Email: andi@mail.com | Telepon: 0812-3456-7890";
   }
</script>
```

**Penjelasan:**

- `document.getElementById("infoKontak")` memilih elemen `<p>` yang akan diisi kontak.
- `info.textContent = ...` mengubah teksnya saat tombol diklik.

**Hasil ketika dijalankan:**

Sekarang tombol `Tampilkan Kontak` akan mengubah teks di halaman dan menampilkan email plus telepon. Portofolio sederhana sudah interaktif.

### Kode Lengkap portofolio.html

```html
<html>
   <head>
      <title>Portofolio Sederhana</title>
      <style>
         body {
            font-family: Arial, sans-serif;
            padding: 20px;
            background-color: #f7f7f7;
         }

         h1 {
            color: #333333;
         }

         .intro {
            max-width: 600px;
            line-height: 1.6;
         }

         .profil {
            display: flex;
            gap: 20px;
            align-items: center;
            margin-top: 20px;
         }

         .profil img {
            width: 120px;
            border-radius: 10px;
            border: 2px solid #cccccc;
         }

         .proyek,
         .pendidikan,
         .kontak {
            margin-top: 30px;
         }

         .card {
            background-color: white;
            border: 1px solid #dddddd;
            padding: 15px;
            border-radius: 8px;
            margin-top: 10px;
         }

         ul {
            list-style-type: disc;
            margin-left: 20px;
         }

         button {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 6px;
            cursor: pointer;
         }

         button:hover {
            background-color: #0056b3;
         }

         #infoKontak {
            margin-top: 10px;
            font-weight: bold;
         }
      </style>
   </head>
   <body>
      <h1>Hai, saya Andi</h1>
      <p class="intro">
         Saya membuat desain web sederhana, proyek kreatif, dan solusi digital
         untuk sekolah.
      </p>

      <div class="profil">
         <img src="gambar/profil.png" alt="Foto Profil" />
         <div>
            <h2>Profil Singkat</h2>
            <p>
               Saya pelajar SMAN 10 yang suka membuat website sederhana dengan
               HTML, CSS, dan JavaScript.
            </p>
         </div>
      </div>

      <section class="proyek">
         <h2>Proyek Unggulan</h2>
         <div class="card">
            <h3>Website Sekolah</h3>
            <p>
               Desain halaman utama sekolah dengan menu, gambar, dan informasi
               profil singkat.
            </p>
         </div>
         <div class="card">
            <h3>Poster Digital</h3>
            <p>
               Membuat poster acara sekolah menggunakan warna, teks, dan ikon
               sederhana.
            </p>
         </div>
      </section>

      <section class="pendidikan">
         <h2>Pendidikan</h2>
         <ul>
            <li>SMAN 10 TAMSEL — Kelas 11 IPA</li>
            <li>Pelatihan HTML & CSS</li>
         </ul>
      </section>

      <section class="kontak">
         <h2>Kontak</h2>
         <p>Klik tombol untuk melihat email dan telepon saya:</p>
         <button onclick="tampilkanKontak()">Tampilkan Kontak</button>
         <p id="infoKontak">-</p>
      </section>

      <script>
         function tampilkanKontak() {
            const info = document.getElementById("infoKontak");
            info.textContent = "Email: andi@mail.com | Telepon: 0812-3456-7890";
         }
      </script>
   </body>
</html>
```

---

## 3. Cara Menjalankan

1. Simpan `portofolio.html` di folder `belajar-html`.
2. Klik kanan pada file, pilih **Open with** → pilih browser (Chrome/Firefox).
3. Halaman akan terbuka dan portofolio siap dilihat.

> 💡 Tidak perlu aplikasi tambahan atau internet — file HTML bisa langsung dibuka dari komputer.
