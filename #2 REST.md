# REST

## Apa itu REST
_REpresentational State Transfer_ (REST) yang merupakan salah satu arsitektur dalam API. Diciptakan oleh **Roy Fielding** pada saat disertasi S3.

## Ilustrasi REST API
REST API dapat dianggap sebagai aktivitas yang ada di sebuah restoran. Dimana analoginya adalah restoran sebagai **REST Server**, customer sebagai **client**, waiter sebagai **API** yang menghubungkan antara _client_ dengan _REST Server_. Lalu terdapat menu sebagai **REST API** yang merupakan sekumpulan aturan pemesanan sehingga **client** tidak dapat sembarangan memesan makanan yang dia inginkan, walaupun sebenarnya **REST Server** memungkinkan untuk memberikan makanan tersebut.
Jadi **API** akan menghubungkan pesanan (**request**) kita ke **REST Server** lalu **API** akan memberikan pesanan (**response**) yang sudah jadi (**JSON**).

## REST Server
Harus ada REST Server
![image](https://user-images.githubusercontent.com/54906064/184538563-653a360d-65cb-4ef4-8796-f9672773fe68.png)
REST Client dapat berupa web, aplikasi mobile, aplikasi desktop, piranti smart home, dan lain-lain.

## REST berbeda dengan RESTful
Di dalam sebuah HTTP terdapat GET (mengambil data) dan POST (menambahkan data). Masih ada HTTP method yang lain misalnya PUT (khusus untuk mengubah data), DELETE (untuk menghapus data), dan lain-lain. Namun PUT dan DELETE tidak dapat dijalankan pada web. Dengan adanya RESTful maka keempat HTTP method tersebut dapat digunakan. Misalkan akan membuat RESTful API, maka dapat menggunakan teknik seperti ini (endpoints):
![image](https://user-images.githubusercontent.com/54906064/184538888-5cdab695-09f3-4354-a12c-36445b12bc67.png)
Dengan menggunakan RESTful maka sekarang harus menggunakan HTTP method yang sesuai dengan penggunaannya, serta nantinya pada URL tidak boleh menggunakan kata kerja (tambahMahasiswa, hapusMahasiswa, ubahMahasiswa, dll), melainkan langsung menggunakan kata benda.

## Stateless
Ketiadaan sebuah state dalam sebuah aplikasi. Setiap request HTTP akan dilakukan secara terisolasi. Server tidak boleh menyimpan state apapun mengenai sesi dari client. Setiap request yang dikirimkan oleh client harus berisi semua informasi yang diminta oleh server, termasuk kemungkinan juga informasi mengenai otentikasi.
Antara satu halaman dengan halaman lain tidak saling berhubungan mengenai data yang dibawa. Misalnya dapat menggunakan cookies, session, atau cara passing variabel lainnya.

## REST
Bisa mengirimkan sebuah program yang executeable (Code on Demand)
