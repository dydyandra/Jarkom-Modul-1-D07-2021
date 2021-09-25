# Laporan Resmi Praktikum Jarkom Modul 1
### Anggota kelompok:
Anggota | NRP | 
------------- | ------------- | 
Amanda Rozi Kurnia | 05111940000094 | 
Dyandra Paramitha W. | 05111940000119 |
Daanii Nabil Ghinannafsi Kusnanta | 05111940000163 |


## Soal 1
### Sebutkan webserver yang digunakan pada "ichimarumaru.tech"! 

Display filter yang digunakan adalah: <br>
`http.host eq “ichimarumaru.tech” 
`
<br>
<br>Setelah memasukkan display filter, dan melakukan _search_, akan muncul paket yang sesuai yaitu dimana _host_ berasal dari "ichimarumaru.tech". 

<img src="images/no1a.png" alt="nomor 1a" width="700">

Pilih paket pertama, klik kanan kemudian **Follow > HTTP Stream.** <br><br>
**Apabila dibuka HTTP Stream:** <Br>
Terlihat bahwa web server yang digunakan yaitu __nginx/1.18.0 (Ubuntu)__
<img src="images/no1b.png" alt="nomor 1b" width="700">

## Soal 2
### Temukan paket dari web-web yang menggunakan basic authentication method!

Display filter yang digunakan adalah: <br>
`http.authbasic`

Adapun setelah memasukkan _display filter_ maka akan muncul paket-paket yaitu: 

<image src="images/no2a.png" alt="nomor 2a" width="700">

## Soal 3
### Ikuti perintah di [basic.ichimarumaru.tech](http://basic.ichimarumaru.tech/)! Username dan password bisa didapatkan dari file .pcapng!
  
## Soal 4
### Temukan paket mysql yang mengandung perintah query select!
  
## Soal 5
### Login ke [portal.ichimarumaru.tech](http://portal.ichimarumaru.tech/) kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap! 
  
## Soal 6
### Cari username dan password ketika melakukan login ke FTP Server!

  
## Soal 7
### Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya `Real.pdf`)

Display filter yang digunakan adalah: <br>
`ftp-data contains Real.pdf`

Kemudian akan muncul paket-paket berikut: <br>
<img src='images/no7a.png' alt="nomor 7a" width="700">

Pilih paket pertama, kemudian **Follow > TCP Stream > Ubah ASCII menjadi RAW > Save As Real.pdf**

Adapun isi dari file tersebut adalah: <br>
<img src='images/no7b.png' alt="nomor 7b" width="700">


## Soal 8
### Cari paket yang menunjukan pengambilan file dari FTP tersebut!
Display filter yang digunakan adalah: <br>
`ftp.request.command==RETR`

Kemudian setelah kita melakukan pencarian menggunakan *display filter*, kita dapat melihat paket-paket yang berkaitan. 

<img src='images/no8a.png' alt="nomor 8a" width="700">

## Soal 9
### Dari paket-paket yang menuju FTP terdapat indikasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama `secret.zip`. Simpan dan buka file tersebut!

## Soal 10
### Selain itu terdapat `history.txt` yang kemungkinan berisi history bash server tersebut! Gunakan isi dari `history.txt` untuk menemukan password untuk membuka file rahasia yang ada di `secret.zip`!

## Soal 11
### Mengambil paket yang berasal dari port 80

## Soal 12
###  Mengambil paket yang mengandung port 21

## Soal 13
### Menampilkan paket yang menuju port 443

Capture Filter:
```
dst port 443
```
  
<img src="https://github.com/dydyandra/Jarkom-Modul-1-D07-2021/blob/master/images/no13a.png" alt="nomor 13a" width="700"> <br>
  
Hasil Capture Filter: <br>
  
<img src="https://github.com/dydyandra/Jarkom-Modul-1-D07-2021/blob/master/images/no13b.png" alt="nomor 13b" width="700"> <br>
  
## Soal 14
### Mengambil paket yang tujuannya [kemenag.go.id](https://kemenag.go.id/)

Capture Filter:
```
dst host kemenag.go.id atau dst host 103.7.13.247
```
  
<img src="https://github.com/dydyandra/Jarkom-Modul-1-D07-2021/blob/master/images/no14a.png" alt="nomor 14a" width="700"> <br>
  
Hasil Capture Filter: <br>
  
<img src="https://github.com/dydyandra/Jarkom-Modul-1-D07-2021/blob/master/images/no14b.png" alt="nomor 14b" width="700"> <br>

## Soal 15
### Mengambil paket yang berasal dari ip kalian
Untuk mendapatkan ip pribadi: Open cmd ketik ```ipconfig``` <br>
ip pada jaringan Wireless LAN adapter Wi-Fi adalah <b>192.168.100.2</b>
  
<img src="https://github.com/dydyandra/Jarkom-Modul-1-D07-2021/blob/master/images/no15a.png" alt="nomor 15a" width="400"> <br>

Capture Filter untuk mengambil paket yang berasal dari ip pribadi: 
```
src host 192.168.100.2
```

<img src="https://github.com/dydyandra/Jarkom-Modul-1-D07-2021/blob/master/images/no15b.png" alt="nomor 15b" width="700"> <br>
  
Hasil Capture Filter: <br>
  
<img src="https://github.com/dydyandra/Jarkom-Modul-1-D07-2021/blob/master/images/no15c.png" alt="nomor 15c" width="700"> <br>
