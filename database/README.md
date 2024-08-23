# Mata Pelajaran Database
## Melihat daftar database yang sudah ada.
Untuk melihat daftar database yang ada pada komputer kita :
> ```SHOW DATABASES;``` ATAU  ``` show databases;```

## Membuat Database
Untuk membuat database syntax umumnya adalah ```CREATE DATABASE <<Nama Database>>``` sebagai contoh kita akan membuat database dengan nama <b> koleksi_buku </b> maka syntax untuk membuatnya adalah sebagai berikut :
>```CREATE DATABASE koleksi_buku; ```

>[!TIP]
>jangan lupa <b>titik koma</b> di setiap akhir perintah
### Untuk menggunakan database yang telah kita buat
>#0000FF ```USE koleksi_buku; ``` 
## Melihat daftar Tabel Membuat Tabel
Untuk membuat tabel syntax umumnya adalah sebagai berikut :
> ```CREATE TABLE <<Nama Table>> (Field_1 DataType(size), Field_2 dataType(size), ..., Field_N dataType(Size)  )```

Sebagai contoh kita akan membuat tabel dengan nama tabelnya **tema** yang memiliki kolom **tema_id** dan **nama** maka syntax yang digunakan adalah
> ```create table tema(tema_id char(3) parimary key , nama varchar(20));```
