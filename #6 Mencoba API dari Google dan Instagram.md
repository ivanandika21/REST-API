# Menggunakan API dari Google dan Instagram

## Google API
Untuk mengakses Google API dapat dilakukan dengan langkah-langkah berikut:
* Masuk ke https://developers.google.com
* Login menggunakan akun gmail
* Persiapkan project : Membuat project di https://console.developers.google.com/
* Klik `Enable APIs and Services`
* Cari YouTube > Klik > Enable
* Membuat API Key : masuk ke Credentials > Pilih API yang sudah di enable tadi
* Klik `What credentials do i need?` > Salin API Key

## Instagram API
Untuk mengakses Instagram API dapat dilakukan dengan langkah-langkah berikut:
* Masuk ke https://www.instagram.com/developer/
* Klik `Register a New Client`
* Isi data :
+ Application Name : nama aplikasi tanpa kata **instagram, IG, insta, atau gram**
+ Deskripsi : Bebas
+ Company Name : Bebas
+ Website URL: isi pakai link localhost aja
+ Valid redirect URIs : sama seperti website URL
+ Privacy Policy URL : : sama seperti website URL
+ Contact email : isi dengan email
* Pindah ke tab Security > Uncheck `Disable implicit OAuth`
* Klik `Register`
* Simpan `Client ID` yang diberikan
* Masuk ke tab `Authentication`
* Scroll sampai ke `Client-Side (Implicit) Authentication`
* Copy URL yang tersedia, ganti `client_id` dengan yang sudah didapatkan sebelumnya, serta ganti `REDIRECT-URL`nya sesuai dengan yang diisikan di awal
* Klik `Authorize`
* Lihat pada bagian url, terdapat `access_token=xxxxxxxxxx`
* 
