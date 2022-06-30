---
title: Mulai Menggunakan
date: Last Modified
permalink: /mulai/
eleventyNavigation:
  key: mulai
  order: 1
  title: Mulai Menggunakan
---

Mulai menggunakan Qore dalam beberapa tahap.

## Langkah Pertama: Menyiapkan Proyek Qore

Buat proyek baru dengan menekan tombol "Create project" tepat setelah registrasi dan login.

![new project](/content/images/Qore-NewProject.png)

## Langkah kedua: Masuk ke Proyek Qore

Masuk ke proyek Qore yang baru dibuat.

![Project Baru](/content/images/Qore-BrandNew.png)

Komponen utama Qore adalah data dalam bentuk tabular atau tabel. Kita dapat menggunakan data tabular tersebut untuk membuat, menghapus ataupun memanipulasi data layaknya _spreadsheet_ ataupun aplikasi Excel. Dan ketika membuat proyek baru secara otomatis sudah menyediakan tabel _default_ yaitu table users. Table users digunakan untuk mengelola pengguna yang akan menggunakan aplikasi yang akan kita buat.

## Langkah ketiga: Membuat Table Baru

Buat sebuah table baru untuk membuat table yang akan menyimpan data dengan menekan tombol "+" diatas table users, pilih "Add new table" dan kita mendapatkan tiga pilihan:

- **Serial primary key** --
- **UUID primary key** --
- **String primary key** --

Namakan table baru dengan "bookmarks".

![New Table](/content/images/Qore-NewTable.png)

### Pemodelan data dengan table

Kolom dapat menyimpan berbagai tipe data seperti bilangan bulat (integer), bilangan desimal (float), _file_, tanggal dan jam, JSON, teks dan banyak lagi.

![Qore Table](/content/images/Qore-Table.png)

### Mengisi Data

Dengan Qore, kita tidak perlu membuat tampilan _back office_ atau _content management_, bisa langsung diisi seperti airtable atau _spreadsheet_.

Untuk memasukkan memasukkan data (insert) dapat dilakukan dengan menekan tombol “Add Row” atau tombol “+”.

Sedangkan untuk mengubah isi data bisa langsung dilakukan dengan mengarahkan kursor ke data yang ingin diubah.

Dam untuk menghapus data dengan mengarahkan kursor ke kolom id dan memilih “Delete this row” atau untuk menghapus seluruh data di table dengan mengarahkan kursor ke header kolom id, centang semua row yang ingin dihapus dan pilih “Delete selected row”.

![Fill Table](/content/images/Qore-FillTable.png)

## Langkah keempat: Memberikan Hak Akses
