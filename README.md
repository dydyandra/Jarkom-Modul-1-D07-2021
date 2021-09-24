# Laporan Resmi Praktikum Jarkom Modul 1
### Anggota kelompok:
Anggota | NRP | Pembagian Soal
------------- | ------------- | -------------
Amanda Rozi Kurnia | 05111940000094 | 
Dyandra Paramitha W. | 05111940000119 | 1,2,7,8
Daanii Nabil Ghinannafsi Kusnanta | 05111940000163


## Soal 
### 1. Sebutkan webserver yang digunakan pada "ichimarumaru.tech"! 

Display filter yang digunakan adalah: <br>
`http.host eq “ichimarumaru.tech” 
`
<br>
<br>Setelah memasukkan display filter, dan melakukan _search_, akan muncul paket yang sesuai yaitu dimana _host_ berasal dari "ichimarumaru.tech". 

<img src="images/no1a.png">

Pilih paket pertama, klik kanan kemudian **Follow > HTTP Stream.** <br><br>
**Apabila dibuka HTTP Stream:** <Br>
Terlihat bahwa web server yang digunakan yaitu __nginx/1.18.0 (Ubuntu)__
<img src="images/no1b.png">

### 2. Temukan paket dari web-web yang menggunakan basic authentication method!

Display filter yang digunakan adalah: <br>
`http.authbasic`

Adapun setelah memasukkan _display filter_ maka akan muncul paket-paket yaitu: 

<image src="images/no2a.png">



### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")

Display filter yang digunakan adalah: <br>
`ftp-data contains Real.pdf`

Kemudian akan muncul paket-paket berikut: 
<img src='images/no7a.png'>

Pilih paket pertama, kemudian **Follow > TCP Stream > Ubah ASCII menjadi RAW > Save As Real.pdf**

Adapun isi dari file tersebut adalah:
<img src='images/no7b.png'>


### 8. Cari paket yang menunjukan pengambilan file dari FTP tersebut!
Display filter yang digunakan adalah: <br>
`ftp.request.command==RETR`

Kemudian setelah kita melakukan pencarian menggunakan *display filter*, kita dapat melihat paket-paket yang berkaitan. 

<img src='images/no8a.png'>

