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

- **Serial primary key** -- kunci unik dalam format angka berurut
- **UUID primary key** -- kunci unik dalam format UUID
- **String primary key** -- kunci unik dalam format teks

Pilih salah satu saja, tidak akan ada masalah untuk aplikasi kita saat ini. Dan namakan table baru dengan "bookmarks".

![New Table](/content/images/Qore-NewTable.png)

### Pemodelan data dengan table

Kolom dapat menyimpan berbagai tipe data seperti bilangan bulat (integer), bilangan desimal (float), _file_, tanggal dan jam, JSON, teks dan banyak lagi.

![Qore Table](/content/images/Qore-Table.png)

### Mengisi Data

Dengan Qore, kita tidak perlu membuat tampilan _back office_ atau _content management_, bisa langsung diisi seperti airtable atau _spreadsheet_.

Untuk memasukkan memasukkan data (insert) dapat dilakukan dengan menekan tombol “Add Row” atau tombol “+”.

Sedangkan untuk mengubah isi data bisa langsung dilakukan dengan mengarahkan kursor ke data yang ingin diubah.

Dan untuk menghapus data dengan mengarahkan kursor ke kolom id dan memilih “Delete this row” atau untuk menghapus seluruh data di table dengan mengarahkan kursor ke header kolom id, centang semua row yang ingin dihapus dan pilih “Delete selected row”.

![Fill Table](/content/images/Qore-FillTable.png)

## Langkah keempat: Memberikan hak akses

Sebelum dapat memanfaatkan data untuk dibaca atau digunakan di aplikasi, kita butuh memberikan hak akses untuk publik. Langsung menuju User setting > User Roles > Public > Table and permission, centang bagian Select untuk table "bookmarks".

![Auth](/content/images/Qore-Authorization.png)

![Auth 2](/content/images/Qore-Authorization-2.png)

## Langkah kelima: Membuat aplikasi dengan App Builder

Qore sudah dilengkapi dengan App builder untuk membangun aplikasi berdasarkan data yang ada. Untuk membuat aplikasi, tekan menu "App" dari menu sebelah kiri layar.

![App Builder](/content/images/Qore-App.png)

Dilanjutkan dengan menekan tombol "Create App" di sebelah kanan layar dan masukkan informasi tentang aplikasi yang ingin dibuat. Pastikan memilih subdomain yang unik yang berbeda dengan yang ada dicontoh. Lanjutkan dengan menekan tombol "Create" di form.

![App Builder](/content/images/Qore-App-2.png)

Dan kita akan diarahkan ke halaman App Builder

![App Builder](/content/images/Qore-App-3.png)

Aplikasi terdiri dari dua bagian: pages dan components. Masing-masing komponen dapat diubah propertinya di sebelah kanan layar. Sedamglam tampilan layar atau preview aplikasi ada di bagian tengah halaman.

Ubah beberapa informasi halaman seperti nama halaman, judul halaman dll.

![Page](/content/images/Qore-App-4.png)

### Tambahkan komponen

Tambahkan komponen List untuk menampilkan data bookmarks kita dengan menekan tombol "+" dibagian "Components".

![component](/content/images/Qore-App-5.png)

Ubah beberapa opsi dengan memilih sumber data, dan menampilkan berbagai field yang diinginkan. Secara otomatis data akan tampil dibagian tampilan atau _preview_.

![preview](/content/images/Qore-App-6.png)


Klik "Save" lalu dilanjutkan dengan "Save & Deploy" untuk meluncurkan aplikasi agar dapat diakses oleh orang banyak.

![deploy](/content/images/Qore-App-7.png)

Akses url aplikasi yang sudah diluncurkan dan lihat hasilnya.

![deploy](/content/images/Qore-App-8.png)