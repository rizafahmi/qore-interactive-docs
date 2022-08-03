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

Lalu kemudian tambahkan kolom baru dengan tipe "relation" dan berikan "bookmarks" sebagai nama kolom. Penamaan kolom sebenarnya bebas, memberikan nama kolom disamakan dengan nama tabel yang akan direlasikan agar memudahkan dan agar konsisten saja.

Untuk konfigurasi relasinya, gunakan "One status Has many bookmarks". Artinya satu status akan dapat memiliki 0 atau lebih banyak bookmarks.

![Kolom relasi](/content/images/tutorial/relation-column.png)

Dan secara otomatis Qore menambahkan `_items` sebagai nama kolom sehingga menjadi "bookmarks_items".

![Kolom relasi](/content/images/tutorial/relation-column-2.png)

Dan secara otomatis kolom ditambahkan di tabel bookmarks sebagai bentuk relasi dengan tabel categories. Dan kita bisa memilih status untuk setiap tautan di tabel bookmark seperti sebelumnya via kolom "bookmarks[status]".

![Kolom relasi](/content/images/tutorial/relation-column-3.png)

Sekarang kita dapat menghitung jumlah tautan yang masuk kedalam kategori _draft_ ataupun _published_ dari tabel status.

Untuk ini kita dapat memanfaatkan tipe kolom "rollup" dengan tipe count.

![rollup](/content/images/tutorial/rollup.png)
