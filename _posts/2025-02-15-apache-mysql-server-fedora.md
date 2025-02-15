---
layout: post
title: Apache, Mysql server, Fedora
date: 2025-02-15 16:15 +0700
---

## Apa itu Apache?
Server HTTP apache atau server web/www apache adalah server web yang dapat dijalankan di banyak sistem operasi yang berguna untuk melayani dan memfungsikan situs web. protokol yang digunakan untuk melayani fasilitas web/www ini menggunakan HTTP. Jadi apache adalah web server yang menangani permintaan client kepada host yang menggunakan apache. dan akan menampilkan isi dari database, (ex: mysql).

## LAMPP
Linux, Apache, Mysql, PHP/Python/Perl (LAMPP) seringkali apache ini disandingkan dengan Mysql. 
Lalu bagaimana cara kerja nya dan kombinasi keduanya? 
Jadi apache adalah gerbang server yang menangani permintaan client dan akan mengirimkan data pada database (mysql). Misalnya sebuah website yang menjual produk sepatu dan menyimpan data menggunakan mysql, maka apache akan mengirimkan data tersebut melalui http/www pada client yang mengakses nya. 

### Install apache di Fedora
Di package Fedora HTTP server dikenal dengan istilah `httpd`. 
install httpd
```terminal
sudo dnf install httpd
```
start apache server
```terminal
sudo systemctl enable httpd.service
```

untuk mengetahui apache sudah berjalan, buka localhost <http://localhost/>, jika berhasil akan menampikan localhost welcome message

root direktori tersimpan di '/var/www/html/'

Seperti di dokumentasi nya, untuk menguji apakah berhasil, bisa  dengan mengkustom halaman localhost. 

### Non Aktifkan Rendering Halaman
yang terletak di `/etc/httpd/conf.d/` atau `/etc/httpd/conf`

```terminal
sudo nano /etc/httpd/conf.d/welcome.conf
```
komentari semua baris dengan `#` dan save.

### Membuat file index baru
Pindah ke direktori:
```terminal
cd /var/www/html
```
Custome `index.html` 

```terminal
sudo nano index.html
```
```bash
<html>
<head>
<title>Selamat Datang</title>
</head>
<body>
<h1>Selamat datang di website saya!</h1>
<p>Ini adalah halaman utama yang baru.</p>
</body>
</html>
```
reload dan lihat hasilnya
```terminal
sudo systemctl reload httpd
```
### Install Mysql Server
```terminal
sudo dnf install @mysql
```
Start Mysql Server dan mengatur berjalan otomatis saat boot
```terminal
sudo systemctl start mysqld
sudo systemctl enable mysqld
```

Konsfigurasi keamanan dan mengatur password root
```terminal
sudo mysql_secure_installation
```
Uji coba akses
```terminal
sudo mysql -u root -p.
```
>gunakan password root yang sudah diatur

## Note
1. Cek status layanan
   ```terminal
   sudo systemctl status httpd
   ```
2. Konfigurasi Firewall (opsional)
   ```terminal
  sudo firewall-cmd --add-service=http --permanent
  sudo firewall-cmd --reload
  ```
3. Menjalankan apache
   ```terminal
sudo systemctl enable httpd.service
```
4. Menjalankan Mysql
```terminal
menjalankan mysql : sudo systemctl start mysqld
```
5. Stop Mysql
   ```terminal
   sudo systemctl stop mysqld
   ```
   ```terminal
  sudo systemctl status mysqld
  sudo systemctl restart mysqld
  sudo systemctl daemon-reload
```

Dokumentasi 
1. <https://developer.fedoraproject.org/start/sw/web-app/apache.html>
2. <https://docs.fedoraproject.org/en-US/quick-docs/getting-started-with-apache-http-server/>
3. <https://docs.fedoraproject.org/en-US/quick-docs/installing-mysql-mariadb/>


