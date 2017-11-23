---
title: "Import data dari Excel ke Mysql"
excerpt: "Cara Import Data Dari Excel Ke Mysql"
header:
  teaser: /assets/images/import-excel-teaser.svg 
  overlay_image: /assets/images/import-excel-teaser.svg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
categories:
  - Tutorial
tags:
  - mysql
  - excel
---
Jadi gini.. temen saya pengen input data dari *spreadsheet* Excel yang jumlahnya
ratusan, *capek* kan kalo input satu-satu lewat aplikasi atau PhpMyAdmin? Ada gak caranya biar datanya bisa di *import* dari Excel? Ternyata bisa! Begini caranya :


## 1. Konversi file Excel anda menjadi .ods
Ini perlu karena PhpMyAdmin tidak support file .xlsx, caranya gampang, cukup save as .ods saja lewat MS-Excel 2010 keatas. 
Jika tidak ada Excel, bisa menggunakan Google Sheet, LibreOffice, WPS Office, atau sesuka anda lah. :smirk:

disini saya akan menggunakan Google Shet, berikut langkahnya:

[Buka Google Sheet](https://docs.google.com/spreadsheets/) (login akun google dulu ya)
kemudian pilih new sheet, tampilannya mirip-mirip lah dengan Excel. 

Asumsikan ada tabel dengan nama `t_mahasiswa` di Mysql dengan struktur seperti ini

|id|nama|jurusan|
|--|----|-------|
auto_increment|varchar|varchar|

begini isi dari file .ods nya :

<figure>
	<a href="/assets/images/step1.png"><img src="/assets/images/step1.png"></a>
</figure>
baris pertama isi dengan nama kolom sesuai dengan kolom pada tabel di database.

Kolom id dikosongkan saja karena `auto_increment`, jika tidak `auto_increment` maka kolom bisa diisi sesuai kebutuhan.

Kemudian pilih `File->Download As->OpenDocument format (.ods)`
<figure>
	<a href="/assets/images/step2.png"><img src="/assets/images/step2.png"></a>
</figure>

## 2. Import File .ods ke PhpMyAdmin
Kemudian buka PhpMyAdmin, pilih database, kemudian table yang ingin di *import* pilih tab *import*
<figure>
	<a href="/assets/images/step2.1.png"><img src="/assets/images/step2.1.png"></a>
</figure>
Selanjutnya :
1. Pilih file .ods
2. Pilih Open Document System
3. Pastikan Ceklis 2 pilihan pertama
4. Tekan Go!!!!!!

Pastikan hasilnya sukses
<figure>
	<a href="/assets/images/success.png"><img src="/assets/images/success.png"></a>
</figure>

Voila! Data telah terisi ke dalam tabel!
<figure>
	<a href="/assets/images/data.png"><img src="/assets/images/data.png"></a>
</figure>

Demikian post ini, semoga bermanfaat.. sekian terima gaji :running:




