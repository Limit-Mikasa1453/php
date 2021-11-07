# Enable oci8 di PHP 8 pada OS Windows
## :seedling:lankah pertama
### - enable extensions oci di `C:\xampp\php\php.ini`
> dengan cara menghapus titik koma `;` jadi  `extension=oci8_12c`
### - donwloads [instantclient](https://www.oracle.com/database/technologies/instant-client/winx64-64-downloads.html) sesuai dengan windows anda
![instantclient](https://user-images.githubusercontent.com/81357488/140661956-db335aae-c5a4-4722-84c4-6cadd22262fd.jpg)
### - extarct dan copy folder `instantclient_21_3` ke partisi C atau D
### - tambahkan `path` ke folder instantclient dengan cara 
  - klik kanan `this pc / my computer` 
  - pilih `properties` 
  - klik `Advanced system settings` 
  - pilih `advanced` 
  - klik `environment variables` 
  - cari groupbox `system variables` 
  - cari variable dan double klik `path` 
  - pilih `button new` 
  - paste ke folder instantclient `C:\instantclient_21_3` 
  - simpan
### jalankan `apache` dan buka [phpinfo](http://localhost/dashboard/phpinfo.php) di browser local komputer, cek apakah oci8 di apache telah enable dengan keywowrd `oci8`, jika sudah `enable` akan seperti gambar dibawah ini. dan jika masih belum bisa coba resart pc dahulu. kalau masih belum bisa lanjutkan ke langkah kedua
![oci8](https://user-images.githubusercontent.com/81357488/140661629-ec1ae1a9-0e50-4428-9dca-4c52fb7ee698.jpg)

## :seedling:langkah kedua
### - download [package oci8](https://pecl.php.net/package/oci8) `dll` sesuaikan dengan `versi php`, arcitecture `x64` or `x86` dan `Non Thread Safety` or `Thread Safety` dengan cek [changalognya](https://pecl.php.net/package-changelog.php?package=oci8&release=3.0.1) 
```
The OCI8 extension lets you access Oracle Database.

Use 'pecl install oci8' to install for PHP 8.

Use 'pecl install oci8-2.2.0' to install for PHP 7.

Use 'pecl install oci8-2.0.12' to install for PHP 5.2 - PHP 5.6.

Use 'pecl install oci8-1.4.10' to install for PHP 4.3.9 - PHP 5.1.
```
![phpinfo](https://user-images.githubusercontent.com/81357488/140661539-b997f9a5-ccd5-4a48-a21b-c56f7d628e13.jpg)
### - copy file semua `.dll` ke `C:\xampp\php\ext`
### - jalankan ulang apache dan cek kembali. `jangan lupa restart pc dulu`


