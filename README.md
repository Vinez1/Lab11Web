# Lab11Web

**Nama : Fery affandi** <br>
**NIM : 312010018** <br>

## Langkah-langkah Praktikum
Sebelum memulai menggunakan Framework Codeigniter, perlu dilakukan konfigurasi
pada webserver.
Beberapa ekstensi PHP perlu diaktifkan untuk kebutuhanpengembangan Codeigniter 4.
Berikut beberapa ekstensi yang perlu diaktifkan:
<br>• php-json ekstension untuk bekerja dengan JSON; <br>
• php-mysqlnd native driver untuk MySQL;<br>
• php-xml ekstension untuk bekerja dengan XML;<br>
• php-intl ekstensi untuk membuat aplikasi multibahasa;<br>
• libcurl (opsional), jika ingin pakai Curl.B=</br>

<br>Untuk mengaktifkan ekstentsi tersebut, melalu <b>XAMPP Control Panel</b>, pada bagian
Apache klik <b>Config -> PHP.ini</b>

![](foto/1.png)
<p align="center">Gambar 11.1 Konfigurasi php

Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan
diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server.

![](foto/2.png)
<p align="center">Gambar 11.2 Ekstensi php

### Instalasi Codeigniter 4

Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara
manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara
manual.

• Unduh Codeigniter dari website https://codeigniter.com/download<br>
• Extrak file zip Codeigniter ke direktori htdocs/lab11_ci.<br>
• Ubah nama direktory framework-4.x.xx menjadi ci4.<br>
• Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/ <br>

![](foto/4.png)

## Menjalankan CLI (Command Line Interface)

Codeigniter 4 menyediakan CLI untuk mempermudah proses development. 
Untuk mengakses CLI buka terminal/command prompt.

![](foto/3.png)

Arahkan lokasi direktori sesuai dengan direktori kerja project dibuat
(xampp/htdocs/lab11_ci/ci4/)

Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah:
``` php
php spark
```

![](foto/5.png)

## Mengaktifkan Mode Debugging

Codeigniter 4 menyediakan fitur <b>debugging</b> untuk memudahkan developer untuk
mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program.

Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan
pesan kesalahan seperti berikut.

![](foto/6.png)

Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis
errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi
pada environment variable <B>CI_ENVIRINMENT</b> menjadi <b>development</b>.

![](foto/7.png)

Ubah nama file <b>env</b> menjadi <b>.env</b> kemudian buka file tersebut dan ubah nilai variable
<b>CI_ENVIRINMENT</b> menjadi <b>development</b>. lalu hapus tanda <b>#</b> sebelum CI_ENVIRINMENT.

Contoh error yang terjadi untuk mencoba error tersebut ubah kode pada file <B>app/Controller/Home.php</b> hilangkan (;) pada akhir kode.

![](foto/9.png)
hasilnya 
![](foto/8.png)

## Membuat Route Baru.

Tambahkan kode berikut di dalam <b>app/Config/Routes.php</b>

```php
$routes->get('/about', 'Page::about');
$routes->get('/contact', 'Page::contact');
$routes->get('/faqs', 'Page::faqs');
```

![](foto/10.png)

Untuk mengetahui route yang ditambahkan sudah benar, buka CLI dan jalankanperintah berikut.

```php
php spark routes
```

![](foto/11.png)

Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost/lab11_php_ci/ci4/public/about

![](foto/12.png)

Ketika diakses akan mucul tampilan error 404 file not found, itu artinya file/page tersebut tidak ada. 
Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.

## Membuat Controller
Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama <b>page.php</b> pada folder 
pada direktori Controller kemudian isi kodenya seperti berikut.

![](foto/13.png)

