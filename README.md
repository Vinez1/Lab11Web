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