

#Map Server 

<p align="center">
  <img src="/img/google_earth_kml_raster.png" width="400px">
</p>

 MapServer adalah sebuah lingkungan pengembangan bersifat sumber terbuka (open source) untuk pengembangan aplikasi internet yang memungkinkan pengolahan spasial. Bisa dijalankan sebagai sebuah program CGI atau melalui Mapscript yang mendukung beberapa bahasa pemrograman. MapServer dulunya dikembangkan oleh Universitas Minnesota. MapServer asalnya dikembangkan dengan dukungan NASA, yang membutuhkan sebuah cara untuk membuat citra satelit mereka bisa tersedia untuk umum.

--Cara install 

1. Jika tidak ada centos maka jalankan saja di virtual box, ISO centos dan virtual box ada di halaman download 

2. Setelah itu pastikan koneksi jaringan virtual box bisa diakses dari komputer host 

3. Dicentos buka terminal, login sebagai root 

4. #install mapserver 

5. Selesai

--Map Proxy adalah program yang berfungsi untuk menampung hasil gambar dari map server agar konsumsi komputer bisa di reduksi

--Cara Install 

1. Install python-pip dan python-dev 

2. #install python-pip dan python-dev 

3. pip Install mapproxy 

4. #install mapproxy 

5. Install Vwsqi 

6. #install Vwsqi

--Testing 

1. Download peta Indonesia beserta map proxy konfigurasinya di Halaman Download simpan di folder/var 

2. Jalankan map proxy dengan cara ketik perintah #vwsqi map proxy ini 

3. Peta seudah bisa diakses di browser localhost

Scan Plagiarism
https://drive.google.com/file/d/0B9frXx67PauPSGZmV2hkeUhhMUk/view