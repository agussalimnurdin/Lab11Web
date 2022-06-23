## Nama =Agus Salim Nurdin

## Nim  =312010494

## kelas =TI.20.B2



# Praktikum 11: PHP Framework (Codeigniter)

# Lab11Web
## Praktikum 11: PHP Framework (Codeigniter)
Buat folder baru lab11_php_ci lalu Jalankan XAMPP Ubah file php.ini seperti berikut :

![gambar 1](screenshot/Screenshot%20(6).png)

Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan 
diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server

![gambar 1](screenshot/Screenshot%20(9).png)

## Instalasi Codeigniter 4
Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara 
manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara 
manual.

Unduh Codeigniter dari website https://codeigniter.com/download
• Extrak file zip Codeigniter ke direktori htdocs/lab11_ci.
• Ubah nama direktory framework-4.x.xx menjadi ci4.
• Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/

![gambar 1](screenshot/Screenshot%20(10).png)

## Buka cmd pada XAMPP Shell lalu buka php spark, untuk menjalankan server ketik "php spark serve" :

![gambar 1](screenshot/Screenshot%20(11).png)


## Mengaktifkan Mode Debugging
Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk 
mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program.

Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan 
pesan kesalahan seperti berikut.

![gambar 1](screenshot/Screenshot%20(15).png)

## Mengaktifkan mode Debugging dengan mengubah file .env menjadi = development, seperti berikut :

![gambar 1](screenshot/Screenshot%20(16).png)

Untuk mencoba Error hilangkan tanda ; (titik koma) pada Home.php, seperti berikut :

![gambar 1](screenshot/Screenshot%20(17).png)

Contoh error/kesalahan akan ditampilkan secara detail

![gambar 1](screenshot/Screenshot%20(18).png)

## Mengarahkan router pada controller, kemudian Membuat Route Baru Tambahkan kode berikut pada Route.php :

![gambar 1](screenshot/Screenshot%20(19).png)

Cek pada CMD dengan memasukan "php spark routes", Akses route yang telah dibuat dengan http://localhost:8080/about, hasilnya :

![gambar 1](screenshot/Screenshot%20(20).png)

Ketika diakses akan mucul tampilan error 404 file not found, itu artinya file/page 
tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih 
dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.

![gambar 1](screenshot/Screenshot%20(21).png)

## Membuat Controller
Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama page.php 
pada direktori Controller kemudian isi kodenya seperti berikut.

![gambar 1](screenshot/Screenshot%20(22).png)

Hasilnya :

![gambar 1](screenshot/Screenshot%20(23).png)

## Auto Routing
Mengaktifkan AutoRouting dengan men set nilai true/false, jika true maka fungsi akan aktif

![gambar 1](screenshot/Screenshot%20(24).png)

Tambahkan method baru pada Controller Page seperti berikut untuk page Term of Services

![gambar 1](screenshot/Screenshot%20(43).png)

Akses http://localhost:8080/page/tos hasilnya :

![gambar 1](screenshot/Screenshot%20(25).png)

## Membuat View
Selanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file 
baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi 
kodenya seperti berikut.

![gambar 1](screenshot/Screenshot%20(27).png)

ubah method about pada class Controller Page menjadi seperti berikut:

![gambar 1](screenshot/Screenshot%20(28).png)

Kemudian lakukan refresh pada halaman tersebut.
hasilnya

![gambar 1](screenshot/Screenshot%20(29).png)

## Membuat Layout Web dengan CSS
Pada dasarnya layout web dengan css dapat diimplamentasikan dengan mudah pada 
codeigniter. Yang perlu diketahui adalah, pada Codeigniter 4 file yang menyimpan asset 
css dan javascript terletak pada direktori public. 

Buat file css pada direktori public dengan nama style.css

![gambar 1](screenshot/Screenshot%20(30).png)

Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php

header.php

![gambar 1](screenshot/Screenshot%20(31).png)

footer.php

![gambar 1](screenshot/Screenshot%20(32).png)

Kemudian ubah file app/view/about.php seperti berikut

![gambar 1](screenshot/Screenshot%20(33).png)

Selanjutnya refresh tampilan pada alamat http://localhost:8080/about

![gambar 1](screenshot/Screenshot%20(34).png)

## Pertanyaan dan Tugas

Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama

Tambahkan kode berikut di dalam Routes.php

![gambar 1](screenshot/Screenshot%20(35).png)

edit page control pada page.php

![gambar 1](screenshot/Screenshot%20(36).png)

Buat file artikel.php dan contact.php pada direktori app/view/.....

![gambar 1](screenshot/Screenshot%20(37).png)

![gambar 1](screenshot/Screenshot%20(38).png)

saat kita membuka halaman artikel dan kontak maka tampilan akan menuju page artikel,about dan kontak 

artikel

![gambar 1](screenshot/Screenshot%20(39).png)

kontak

![gambar 1](screenshot/Screenshot%20(40).png)

about

![gambar 1](screenshot/Screenshot%20(41).png)




# Praktikum 12: Framework Lanjutan (CRUD)
## Membuat Database
CREATE DATABASE lab_ci4;
Membuat Tabel

seperti gambar berikut

![gambar 1](screenshot/Screenshot%20(45).png)

Jalankan MySQL pada program XAMPP berjalan dan buat database seperti berikut :

![gambar 1](screenshot/Screenshot%20(46).png)

## Konfigurasi koneksi database
Mengkonfigurasi koneksi database pada file .env seperti berikut :

![gambar 1](screenshot/Screenshot%20(70).png)

## Membuat Model
Membuat file Model pada direktori app/Models dengan nama ArtikelModel.php seperti berikut :

![gambar 1](screenshot/Screenshot%20(47).png)

## Membuat Controller
Membuat file Controller baru dengan nama Artikel.php pada direktori app/Controllers. seperti berikut :

![gambar 1](screenshot/Screenshot%20(48).png)

## Membuat View
Membuat file Views baru dengan nama artikel pada direktori app/views, kemudian buat filebaru dengan nama index.php, seperti berikut 

![gambar 1](screenshot/Screenshot%20(49).png)

Jalankan server dan akses link : http://localhost:8080/artikel

hasilnya

![gambar 1](screenshot/Screenshot%20(50).png)

Masukan data berikut pada database :

![gambar 1](screenshot/Screenshot%20(51).png)

Refresh kembali browser, sehingga akan ditampilkan hasilnya.

![gambar 1](screenshot/Screenshot%20(52).png)

## Membuat Tampilan Detail Artikel
Menambahkan Detail pada Artikel.php seperti berikut :

![gambar 1](screenshot/Screenshot%20(53).png)

## Membuat View Detail
Membuat file baru baru untuk halaman detail dengan nama app/views/artikel/detail.php. seperti berikut :

![gambar 1](screenshot/Screenshot%20(54).png)

Tambahkan rute baru pada Routes.php :

![gambar 1](screenshot/Screenshot%20(55).png)

Tampilan Artikel setelah di Klik :

![gambar 1](screenshot/Screenshot%20(56).png)

## Membuat Menu Admin
Buat method baru pada Controller Artikel dengan nama admin_index() :

![gambar 1](screenshot/Screenshot%20(57).png)

Buat file baru dengan nama admin_index.php pada folder artikel :

![gambar 1](screenshot/Screenshot%20(58).png)

![gambar 1](screenshot/Screenshot%20(59).png)

Tambahkan Routing baru pada Routes.php seperti berikut :

![gambar 1](screenshot/Screenshot%20(60).png)

Akses menu admin dengan url http://localhost:8080/admin/artikel :

hasilnya

![gambar 1](screenshot/Screenshot%20(61).png)

## Menambah Data Artikel
Tambahkan fungsi/method baru pada Controller Artikel dengan nama add() :

![gambar 1](screenshot/Screenshot%20(62).png)

Lalu buat file baru dengan nama form_add.php pada folder artikel :

![gambar 1](screenshot/Screenshot%20(63).png)

tampilan saat klik artikel :

![gambar 1](screenshot/Screenshot%20(64).png)

## Mengubah Data artikel
Tambahkan fungsi/method baru pada Controller Artikel dengan nama edit() :

![gambar 1](screenshot/Screenshot%20(65).png)

Lalu buat file baru dengan nama edit_add.php pada folder artikel :

![gambar 1](screenshot/Screenshot%20(67).png)

Tampilan saat mengubah artikel :

![gambar 1](screenshot/Screenshot%20(68).png)

## Menghapus Data
Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete().

![gambar 1](screenshot/Screenshot%20(69).png)

## Pertanyaan dan Tugas
Selesaikan programnya sesuai Langkah-langkah yang ada. Anda boleh melakukan 
improvisasi

jawab

mohon maaf pak belum sampai ilmunya pak



# Praktikum 13: Framework Lanjutan (Modul Login)














