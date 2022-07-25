---
title: 3️⃣ Relasi Antar Tabel
date: Last Modified
permalink: /tutorial/ch3/index.html
eleventyNavigation:
  parent: Tutorial
  key: ch2
  order: 2
  title: 3️⃣ Relasi Antar Table
---

Saat ini kolom `status` masih statis dengan tipe _select_ sehingga kurang fleksibel. Jika ada kebutuhan untuk mengetahui jumlah tautan yang statusnya masih konsep atau _draft_ atau yang sudah dipublikasikan belum bisa dilakukan.

Agar dapat melakukan hal seperti itu kita bisa buatkan tabel terpisah untuk status dan menghubungkan tabel `bookmarks` dengan tabel `status`.

Kita buat sebuah tabel baru dengan nama "status" untuk menampung semua informasi tentang status.

![Tabel Status](/content/images/tutorial/table-status.png)

Lalu kemudian tambahkan kolom baru dengan tipe
