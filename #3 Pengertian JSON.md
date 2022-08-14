# Pengertian JSON

## Apa itu JSON?
_Javascript Object Notation_ (JSON) adalah sebuah standar format file menggunakan tulisan yang dapat dibaca oleh manusia untuk melakukan pertukaran data yang mengandung pasangan antara key dan value. JSON merupakan format pertukaran data yang sangat simpel, sederhana, dan jelas untuk dibaca. JSON dapat digunakan dalam berbagai bahasa pemrogaman, jadi berbagai API dari bahasa pemrograman dapat menggunakan JSON.
JSON dibuat berdasarkan format Object pada Javascript. JSON juga dapat digunakan sebagai file konfigurasi (tidak disarankan, karena JSON tidak dapat mengandung sintaks komentar, padahal biasanya pada file konfigurasi diperlukan komentar)
Formatting menggunakan JSON ini diusulkan oleh Douglas Crockford.

## JSON vs XML
Cara membuat JSON adalah sebagai berikut:
```
{
  "mahasiswa" :
    [
      {
        "nama" : "Ivan Andika Surya",
        "nim" : "672019171",
        "progdi" : "Teknik Informatika"
      },
      {
        "nama" : "Surya Andika Ivan",
        "nim" : "672019123",
        "progdi" : "Sistem Informasi"
      }
    ]
}
```

Sedangkan jika menggunakan XML maka perlu menuliskan sebagai berikut:
```
<fti>
  <mahasiswa>
    <nama>Ivan Andika Surya</nama>
    <nim>672019171</nim>
    <progdi>Teknik Informatika</progdi>
  </mahasiswa>
  <mahasiswa>
    <nama>Surya Andika Ivan</nama>
    <nim>672019123</nim>
    <progdi>Sistem Informasi</progdi>
  </mahasiswa>
</fti>
```

## Object Literal
Ketika memmbuat object dalam Javascript misalnya:
```
var Mahasiswa = {
  nama : "Ivan Andika Surya",
  umur : 21,
  nim : "672019171",
  sapa : function() {
         "Halo, nama saya " + this.nama +
         " umur saya " + this.umur +
         " tahun, dan nim saya adalah " + this.nim;
  }
}
```

## Membuat JSON
Dalam membuat JSON akan selalu ada ```{ "key" : "value" }```
**key** selalu dibungkus menggunakan petik ("key")
**value** dapat diisi dengan berbagai macam tipe data: boolean, array, string, number, object (yang berisi ```{ "key" : "value" }``` lagi), dan null 
> disingkat BASNON

# PHP
## Sintaks penting untuk JSON di PHP
Dari array menjadi JSON maka menggunakan fungsi ```json_encode()```
Sedangkan dari JSON ke array menggunakan fungsi ```json_decode()```

## Mengakses JSON berupa file
Menggunakan ```file_get_contents()```
```
$contents = file_get_contents('data.json');
$contents = utf8_encode($contents);

// jika parameter kedua diisi dengan true maka mengubah string json menjadi array associative
$result = json_decode($contents, true)
```
## Mencoba JSON di PHP
### json_encode()
Proses **encode** dari array menjadi JSON:
```
<?php
$mahasiswa = [
    [
        "nama"  => "Ivan Andika Surya",
        "umur"  => 21,
        "nim"   => "672019171"
    ],
    [
        "nama"  => "Surya Andika Ivan",
        "umur"  => 22,
        "nim"   => "672019123"
    ]
];

$data = json_encode($mahasiswa);
echo($data);
?>
```
Atau ambil dari database:
```
<?php
$dbh = new PDO('mysql:host=localhost; dbname=phpdasar', 'root', 'root');
$db = $dbh->prepare('SELECT * FROM mahasiswa');
$db->execute();
$mahasiswa = $db->fetchAll(PDO::FETCH_ASSOC);

$data = json_encode($mahasiswa);
echo($data);
?>
```
### json_decode()
Proses **decode** dari JSON menjadi array
```
<?php
$contents = file_get_contents('coba.json');
$result = json_decode($contents, true);

var_dump($result);
echo $result[0]["pembimbing"]["pembimbing1"];
?>
```

# Javascript
## Sintaks penting untuk JSON di PHP
Dari object menjadi JSON maka menggunakan fungsi ```JSON.stringify()```
Sedangkan dari JSON ke object menggunakan fungsi ```JSON.parse()```

## Cara mengakses JSON dalam Javascript
* ajax
+ XMLHttpRequest
+ JQuery

### JSON.stringify()
Mengubah object javascript menjadi JSON
```
var data = {
  a : '1',
  b : '2',
  c : '3'
}

console.log(JSON.stringify(data));
```

