---
layout: post
image: 
title: Tutorial Install Nodejs Di Linux
post_id: 1
author_name: Unang
author_id: 1
featured: true
date: 2020-01-03 8:14:30 +0600
tags: [Linux]
categories: [Tutorial]
post_image: https://nodejs.org/static/images/logos/nodejs-new-pantone-black.svg
---

Node.js adalah platform yang dibangun di atas JavaScript engine<!--more--> V8 Chrome. Node.js dapat digunakan untuk dengan mudah 
untuk membangun aplikasi jaringan yang cepat dan memiliki skalabilitas yang tinggi. Versi terbaru ppa node.js dikelola oleh situs web resminya. 
Sehingga untuk mulai instalasi harus menambahkan PPA ini ke sistem Debian 10 (Buster), Debian 9 (Stretch) Debian 8 (Jessie) dan Debian 7 (Wheezy). Pada tutorial ini kita akan menambahkan ppa sekaligus menginstal Nodejs &amp; NPM terbaru pada sistem Debian 10/9/8/7.

<center><img class="aligncenter size-full wp-image-5155 td-animation-stack-type0-2" src="https://cdn.linuxid.net/assets/media/img_5d0fdf03bedbf.png" alt="Install nodejs" width="500" height="250"/></center>

#Langkah 1 – Tambahkan Node.js PPA
kamu wajib untuk menambahkan Node.js PPA ke sistem, PPa ini disediakan oleh situs web resmi Nodejs. Kita juga perlu menginstal paket software-properties-common jika belum diinstal. kamu dapat memilih untuk menginstal versi Node.js terbaru atau versi LTS.

<strong>Untuk Rilis Terbaru :</strong>
<pre>sudo apt-get install curl software-properties-common
curl -sL https://deb.nodesource.com/setup_12.x | sudo bash -
</pre>
<strong>Untuk Rilis LTS (Long Term Support)</strong>
<pre>sudo apt-get install curl software-properties-common
curl -sL https://deb.nodesource.com/setup_10.x | sudo bash -
</pre>

#Langkah 2 – Install Node.js di Debian Linux
Setelah menambahkan file PPA yang diperlukan, mari kita instal paket Nodejs. NPM juga akan diinstal dengan node.js. Perintah ini juga akan menginstal banyak paket dependen lainnya di sistem kamu.

<pre>sudo apt-get install nodejs</pre>

#Langkah&nbsp;3 – Periksa Versi Node.js
Setelah menyelesaikan instalasi, periksa dan verifikasi versi Node.js dan NPM yang diinstal. kamu dapat menemukan detail lebih lanjut tentang versi saat ini di <a href="https://nodejs.org/download/" target="_blank" rel="noopener">situs web resmi node.js</a>.
<pre>node -v</pre><br/>
<pre>npm -v</pre>
#Opsional – Membuat Demo Web Server
Ini merupakan langkah opsional. Jika kamu ingin menguji instalasi node.js kamu. Mari kita membuat server web dengan teks “Hello World!”. Buat file <strong>http_server.js</strong>
<pre>vim http_server.js</pre>
dan kemudian tambahkan konten berikut
<pre>var http = require('http');
http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World\n');
}).listen(3000, "127.0.0.1");
console.log('Server running at http://127.0.0.1:3000/');
</pre>
Kemudian jalankan web server menggunakan perintah.
<pre>node http_server.js

Server running at http://127.0.0.1:3000/
</pre>
Web server telah berhasil berjalan di port 3000. kamu dapat mengakses&nbsp;url &nbsp;<strong>http://127.0.0.1:3000/</strong>&nbsp;di web browser.
