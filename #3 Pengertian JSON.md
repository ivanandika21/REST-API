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
