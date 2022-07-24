---
title: 2️⃣ Proyek Qore
date: Last Modified
permalink: /tutorial/ch2/index.html
eleventyNavigation:
  parent: Tutorial
  key: ch2
  order: 2
  title: 2️⃣ Proyek Qore
---

Setelah membuat proyek baru, dan masuk kedalamnya dengan memilih proyek yang baru dibuat dari dashboard, akan muncul tampilan seperti berikut. Proyek Qore memiliki menu di sebelah kiri yang terdiri dari Data (Table), Apps, Pipeline, API Docs dan Setting.

![Empty Project](/content/images/Qore-Tutorial--EmptyProject.png)

Ketika pertama kali membuka proyek Qore, maka secara otomatis kita akan berada di menu Data, yang merupakan komponen utama dari Feedloop Qore. Kita dapat memanipulasi data layaknya _spreadsheet_ dengan cara membuat tabel baru dan memanipulasi data didalamnya.
Proyek Qore sudah menyediakan tabel pertama yaitu tabel users atau pengguna. Tabel users dapat digunakan untuk mengelola pengguna yang akan menggunakan aplikasi yang akan kita buat. Kita akan membahas tentang tabel users ini nanti di bagian yang lain.

## Membuat Tabel Baru

Untuk membuat tabel yang akan menyimpan data dapat dilakukan dengan menekan tombol "+" ketika di menu Data. Kita mendapatkan tiga pilihan:

- **Serial primary key** -- kunci unik dalam format angka berurut
- **UUID primary key** -- kunci unik dalam format UUID
- **String primary key** -- kunci unik dalam format teks

![New Table](/content/images/Qore-Tutorial--TableNew.png)

Dan berhubung kita tidak atau belum akan menggunakan kunci unik dalam aplikasi, kita akan pilih yang paling sederhana yaitu Serial Primary Key saja.

Kita akan membuat aplikasi untuk menyimpan informasi menarik yang didapat dari internet. Data yang akan disimpan diantaranya adalah judul, deskripsi, tautan dan lain sebagainya.

Untuk nama tabel kita berikan saja "bookmarks" sebagai nama tabelnya dan siapkan kolom beserta tipe data seperti berikut:

- **title** dengan tipe text
- **description** dengan tipe text
- **url** dengan tipe text dan tambahkan opsi unik (unique) 
- **date_published** dengan tipe datetime
- **status** dengan tipe select beserta beberapa pilihan status

![Qore Table Status](/content/images/Qore-Table--Status.png)

Berikut keseluruhan struktur tabelnya.

![Qore Table Structure](/content/images/Qore-Table--Fields.png)

## Memasukkan Data

Mari sekarang kita masukkan beberapa data kedalam tabel "bookmarks" yang baru saja dibuat. Untuk memasukkan data kedalam tabel bisa dilakukan dengan menekan tombol "+ Add Row" dibagian atas tabel ataupun tombol "+" dibagian bawah tabel.

![Add Row](/content/images/Qore-Table--Add-Row.png)
