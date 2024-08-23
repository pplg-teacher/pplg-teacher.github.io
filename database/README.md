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

1. Tabel tema
> ```create table tema(tema_id char(3) parimary key, nama varchar(20));```

2. Tabel negara
> ```create table negara(negara_id char(2) primary key, nama_neg_penulis  varchar(30));```

3. tabel buku
<code>
create table buku (
  buku_id int(5) unsigned primary key auto_increment,
  judul varchar(50),
  tema_id char(3),
  bahasa varchar(15),
  isbn varchar(20),
  tahun_cetak year(4) default '0000',
  harga_beli int(11) default '0',
  tanggal_beli date default current_date,
  jumlah_hal int(4) unsigned,
  jenis_sampul enum('HC','SC') default 'HC',
  jenis_kertas enum('B','H') default 'B',
  sinopsis varchar(255),
  keterangan varchar(255)
);
</code>

5. tabel penulis
6. tabel penerbit
7. tabel buku_penerbit
8. tabel buku_penulis
