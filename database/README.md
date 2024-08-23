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
> <code>
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

MariaDB [koleksi_buku]> desc penulis;
+------------+-----------------+------+-----+---------+----------------+
| Field      | Type            | Null | Key | Default | Extra          |
+------------+-----------------+------+-----+---------+----------------+
| penulis_id | int(4) unsigned | NO   | PRI | NULL    | auto_increment |
| nama       | varchar(50)     | YES  |     | NULL    |                |
| kelamin    | enum('P','L')   | YES  |     | P       |                |
| alamat     | varchar(50)     | YES  |     | NULL    |                |
| kota       | varchar(40)     | YES  |     | NULL    |                |
| kodepos    | varchar(5)      | YES  |     | NULL    |                |
| propinsi   | varchar(20)     | YES  |     | NULL    |                |
| negara_id  | char(2)         | YES  |     | NULL    |                |
| website    | varchar(25)     | YES  |     | NULL    |                |
| email      | varchar(25)     | YES  |     | NULL    |                |
| telepon    | varchar(20)     | YES  |     | NULL    |                |
| keterangan | varchar(255)    | YES  |     | NULL    |                |
+------------+-----------------+------+-----+---------+----------------+
<code>
create table penulis (
  penulis_id int(4) unsigned primary key auto_increment,
  nama varchar(50),
  kelamin enum('P','L') default 'P',
  alamat varchar(50),
  kota varchar(40),
  kodepos varchar(5),
  propinsi varchar(20),
  negara_id char(2),
  website varchar(25),
  email varchar(25),
  telepon varchar(20),
  keterangan varchar(255)
);
</code>

7. tabel penerbit
8. tabel buku_penerbit
9. tabel buku_penulis
