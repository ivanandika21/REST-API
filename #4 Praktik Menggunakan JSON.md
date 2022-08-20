# Praktik Menggunakan JSON

## PHP
Dalam kondisi memiliki file JSON maka untuk membaca menjadi sebuah halaman web dapat dituliskan sebagai berikut:
```
<?php
$data = file_get_contents('data/menu.json');
$data = json_decode($data, true);
$menu = $data["menu"];
?>
```
Lalu setelah mendapatkan semua data berupa array associative, maka dapat menggunakan perulangan foreach untuk menampilkan setiap index yang tersedia.

## JS
Dalam kondisi memiliki file JSON maka untuk membaca menjadi sebuah halaman web dapat dituliskan juga menggunakan JQuery sebagai berikut:
```
$.getJSON('data/menu.json', function(data){
  let menu = data.menu;
  
  $.each(menu, function(i, data){
    $('#daftar-menu').append('ini nama gambarnya: ' + data.gambar + "terus ini nama menunya: " + data.nama); // ibaratkan pada html sudah dipersiapkan sebuah elemen dengan id = daftar-menu
  });
});
```

## Sebagai tambahan, WPU juga ngajarin tentang JQuery untuk membuat kategori menu
https://youtu.be/UNjknizL2EI?t=1858
