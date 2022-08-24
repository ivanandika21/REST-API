* API : Application Programming Interface
* Interface : antarmuka, merupakan penghubung antara dua atau lebih komponen terpisah
* REST : Representational State Transfer
* HTTP : Protokol yang digunakan untuk melakukan request dan response
* URL : Uniform Resource Locator (alamat untuk mengakses sumber daya)
* Resource : sumber daya, bisa berupa gambar, file, teks html, css, dan lain-lain
* JSON : Javascript Object Notation
* Object : Pada Javascript, object merupakan kumpulan properti yang ditulis dalam pasangan key dan value
* Same-Origin Policy : Aturan browser untuk menampilkan atau mengakses data dari server yang berbeda, sehingga tidak diperkenankan mengambil data (.json) dari luar domain atau domain yang berbeda
![image](https://user-images.githubusercontent.com/54906064/185731781-f33a6cdc-2d62-4e09-bb12-6057a1716f5a.png)
* CORS : Cross Origin Resource Sharing, mekanisme yang membuat kita dapat mengakses data dari server/domain yang berbeda dengan cara mengubah konfigurasi **Access-Control-Allow-Origin** yang biasanya terdapat pada .htaccess. Caranya adalah sebagai berikut:
```
<IfModule mod_headers.c>
  Header set Access-Control-Allow-Origin "*"
</IfModule>
```
* Public API : Sering juga disebut sebagai Open API, adalah API yang dapat diakses secara publik, yang didalamnya terdapat aturan untuk developer agar dapat mengakses data didalamnya.
* Key/Token : Digunakan sebagai otentikasi untuk membatasi pengguna dari sebuah API
* 
