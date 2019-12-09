---
layout: post
title: Mengenal environment PHP
author: admin
categories:
- web programming
- php
image: "/uploads/1_PSPGpssNRDAtETP3erLQhA.png"
tags: php, web

---
Oke kawan-kawan, sekarang kita ada di materi mengenal environment PHP. begitulah ya..  
jadi sebelum kawan memulai ngoding, ane jelasin dulu untuk apa kita belajar PHP? Menurut survei dari [stackoverflow,](https://insights.stackoverflow.com/survey/2018/) PHP berada di peringkat 9 dari 25 bahasa pemrograman terpopuler untuk kategori _most popular technologies_.

![](/uploads/1_PSPGpssNRDAtETP3erLQhA.png)

Itu artinya, kita masih ada harapan untuk belajar pemrograman PHP. kalau menurut saya, belajar pemrograman itu tergantung kebutuhannya untuk apa. PHP emg tertinggal karena peringkatnya 9, tapi seluruh dunia masih banyak yang menggunakan PHP sebagai pemrograman server side dan itu masih layak untuk dipelajari.

Menurut [wikipedia](https://id.wikipedia.org/wiki/PHP).. **_PHP: Hypertext Preprocessor_** adalah [bahasa skrip](https://id.wikipedia.org/wiki/Bahasa_skrip) yang dapat ditanamkan atau disisipkan ke dalam [HTML](https://id.wikipedia.org/wiki/HTML). PHP banyak dipakai untuk memprogram [situs web](https://id.wikipedia.org/wiki/Situs_web) dinamis. PHP dapat digunakan untuk membangun sebuah [CMS](https://id.wikipedia.org/wiki/CMS).

Ada kata:: “Situs web dinamis”, berarti PHP ini adalah sebuah pemrograman yang selalu berinteraksi dengan proses atau pemrograman sisi server.

Apa itu _server side?_ _server side programming languange_ adalah bahasa pemrograman web yang berjalan di sisi server. berbeda dengan yang sudah teman-teman pelajari seperti HTML, CSS, maupun js, mereka dapat bekerja di sisi klien atau _Client Side_.

Jika kita berbicara tentang _Client Side_, sisi klien ini yang akan berhubungan dengan pengunjung web, atau bisa dibilang teknik pemrograman yang kita buat itu bisa dilihat sama pengunjung, berbeda dengan sisi server. kalau sisi server, sederhananya, pengunjung gak akan tau proses apa yang terjadi di dalamnya. user cuma tau kalo klik ini gimana ya.. klik itu ngapain ya.. tapi prosesnya tidak tau.

Contoh: kalian kan pernah membuat sebuah form registrasi, nah form registrasi itu kan bisa dilihat sama pengunjung / user / pengguna. tapi kalau misal form itu kita taruh atau kita tambah dengan kode program PHP, form itu dapat menjadi dinamis, kita bisa registrasiin siapa saja, misal.. ada kalo input nomor hp, tapi kita input huruf, dia keluar pesan “error”, tapi kalo kita input angka, dia akan keluar pesan “berhasil”. hal ini di proses di sisi server, nanti pesan itu ditampilkan di sisi klien menggunakan bantuan pemrograman sisi klien ( html, css, js, dll)

Itu secara umum perbedaan sisi server dan klien, semoga paham. kalo ga paham bisa kasih tau di komentar.

Menurut **DuniaIlkom**, Selain server side, ada juga namanya

1. file server — menyimpan dan berbagi pakai file
2. database server — menyimpan dan menampilkan data
3. email server — menyimpan dan mengatur lalu lintas email
4. web server — memproses dan menangani perminataan halaman website

secara fisik, server ini hanyalah komputer biasa dengan berbagai komponen-komponen. misal menggunakan prosesor khusus untuk server, Ram untuk kebutuhan server, maupun media penyimpanan (_Harddisk)._

nah, untuk mengubah sebuah komputer yang teman-teman pake menjadi server, kita perlu install aplikasi khusus untuk server. contoh: untuk database server kita butuh MySQL, dan untuk Web Server, tersedia aplikasi _apache, nginx_ (baca: bukan njinx ya, tapi engine X cara bacanya).

**Web server** ini lah yang diperlukan untuk menjalankan kode program PHP.  
ada banyak Webserver seperti xampp, wamp, l**aragon**.. tapi nanti kita pake **laragon** aja ya 😾. lanjut..

Sekarang.. kita harus tau bagaimana kode program php bekerja.

![](/uploads/0_hV4QwQr0msvmEnqI.gif)

sumber :: Gambar google

stepnya..

1. Klien sebut saja mawar, mawar mau buka menu **kontak..** oke mawar klik kontak.. nah berarti mawar sedang minta ke server terkait permintaan bukan dong halaman kontak. permintaan tersebut akan dikirim kepada web server. web server kemudia ngecek, file apaan sih yang diminta.. karena file yang diminta berisi kode PHP, maka **web server** manggil2in modul-modul PHPnya dan melakukan pemrosesan sesuai dengan aturan php.
2. Nah kalo file kontak tersebut berisi record-record atau data yang ada di db, maka file php melakukan koneksi dengan **database server**, yakni contohnya MySQL.
3. Nah Database server ini akan merespon dan memproses permintaan php dan mengirimkan hasilnya (GET nanti namanya). Proses php akan terkoneksi ke db karena permintaan user, ntah dia mau insert data, mau lihat datanya aja, mau hapus data, mau ubah data. nah perintah-perintah insert, baca data, hapus data, ubah data itu ditulis menggunakan skrip PHP. karena yang bisa koneksi dengan DB itu salah satunya PHP..
4. nah data-data yang diminta sama user kan ada ya, tersedia di **db**. maka **db** akan ngirim hasilnya ke **php**, dan **modul php** akan nyerahin hasilnya itu kepada **web server..**
5. Nah webserver ini yang akan generate hasil tersebut dan disampaikan kepada user dalam bentukan baik HTML, CSS, JS.

contoh singkatnya::  
Mawar: sisi client  
Dinda: sisi server  
dompet: DB

Mawar: “bro, duit lu ada berapa?”;  
dinda: “ntar dulu gua cek di dompet”;  
Dompet: “2rb”;  
dinda lalu get data dari dompet, terus kasih tau ke mawar..  
Mawar: “war, cuma ada 2rb”;  
Seketika informasi tersebut akan dijadikan pengambilan keputusan si mawar.

Berarti..  
jika kita ingin menjalankan kode PHP, kita butuh yang namanya Editor ya..  
kita pake  
1\. [Visual Studio Code](https://code.visualstudio.com/) — sebagai editonya  
2\.[ Laragon](https://laragon.org/) — sebagai webservernya  
3\. [Browser Firefox / Chrome](https://www.mozilla.org/id/firefox/new/) — Biar kita bisa komunikasi dengan sistem, butuh tampilan..

PR nya.. teman-teman install aja ketiganya.. komen kalo udah instalasi / jika terjadi kendala.

buat akun medium dulu, karena informasi di medium bagus-bagus..

Sekian ya :).

Lampiran : [https://medium.com/@alfinchandra4/mengenal-environment-php-5ffa7ebff3ef](https://medium.com/@alfinchandra4/mengenal-environment-php-5ffa7ebff3ef "https://medium.com/@alfinchandra4/mengenal-environment-php-5ffa7ebff3ef")

**_Artikel ini hanya demo untuk percobaan blog jekyll_**