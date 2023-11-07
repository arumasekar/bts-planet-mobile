# bts_planet_mobile

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

## TUGAS PBP

# Tugas 7
1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?

- Stateless widgets adalah widgets yang tidak berubah. Tampilan dan propertinya tetap tidak berubah sepanjang masa pakai widget. Sederhananya, widget Stateless tidak dapat mengubah statusnya selama runtime aplikasi, yang berarti widget tidak dapat digambar ulang saat aplikasi sedang berjalan.
Contoh: Icon, IconButton, dan Text adalah contoh widget stateless.

- Stateful widgets adalah widget yang mengubah propertinya selama run-time. Mereka bersifat dinamis, yaitu dapat berubah dan dapat ditarik berkali-kali selama berjalan. Hal itu dapat mengubah tampilannya sebagai respons terhadap peristiwa yang dipicu oleh interaksi pengguna atau ketika menerima data.
Contoh : Checkbox, Radio Button, Slider, InkWell, Form, dan TextField adalah contoh widget Stateful.

2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.

- MyHomePage adalah komponen tampilan utama aplikasi yang tidak memiliki keadaan internal dan bertanggung jawab untuk menampilkan daftar item kepada pengguna.

- Scaffold adalah sebuah kerangka tampilan utama yang digunakan untuk mengatur elemen-elemen dasar seperti AppBar dan body dari halaman.

- AppBar adalah bagian atas halaman yang berisi judul aplikasi, menampilkan informasi tentang konten halaman.

- Text adalah widget yang digunakan untuk menampilkan teks, dalam hal ini, judul "BTS Planet Shop" yang menjadi judul aplikasi.

- SingleChildScrollView adalah widget yang memungkinkan kontennya untuk dapat di-scroll jika melebihi ukuran layar, memungkinkan pengguna untuk melihat seluruh kontennya.

- Padding adalah widget yang menambahkan ruang kosong atau padding ke sekitar kontennya, memungkinkan tampilan yang lebih rapi.

- Column adalah widget yang mengatur elemen-elemen anak secara vertikal, memungkinkan penataan konten dengan mudah.

- GridView.count adalah widget yang digunakan untuk menampilkan daftar item toko dalam bentuk grid, dengan jumlah kolom yang ditentukan.

- ShopItem adalah kelas model yang mendefinisikan item toko dengan atribut seperti nama, ikon, dan warna.

- ShopCard adalah widget yang digunakan untuk menampilkan setiap item toko dalam bentuk kartu, termasuk latar belakang yang menggunakan warna dari ShopItem, ikon, dan teks.

- Material adalah widget yang memberikan latar belakang berwarna sesuai dengan ShopItem dan membuat area item responsif terhadap sentuhan pengguna.

- InkWell adalah widget yang memberikan respons ketika item toko ditekan, dalam hal ini menampilkan pesan pop-up SnackBar.

- Icon adalah widget yang menampilkan ikon yang mewakili item toko.

- SnackBar adalah widget yang menampilkan pesan pop-up sementara ketika item toko ditekan.

- MyApp adalah komponen yang menginisialisasi aplikasi dan menentukan tema dasar dan halaman utama aplikasi.

- MaterialApp adalah widget yang mengatur konfigurasi dasar aplikasi, termasuk tema, dan halaman utama aplikasi, dan merupakan titik masuk aplikasi Flutter.

3.  Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)

1) Langkah 1: Merapikan Struktur Proyek

- Membuat file baru bernama menu.dart di direktori bts_planet_mobile/lib.
- Pindahkan (cut) kode MyHomePage dan _MyHomePageState dari main.dart ke menu.dart.
- Import file menu.dart di awal main.dart untuk mengakses kembali MyHomePage.

2) Langkah 2: Mengubah Warna Tema Aplikasi

- Buka file main.dart.
- Mengubah tema warna aplikasi menjadi biru, ungu, dan merah dengan menambahkan konfigurasi colorScheme yang mengacu pada Colors.color.

3) Langkah 3: Mengubah Widget Halaman Menu Menjadi Stateless

- Pada main.dart, menghapus MyHomePage(title: 'Flutter Demo Home Page') dan menggantinya dengan MyHomePage().
- Pada menu.dart, mengubah sifat widget MyHomePage dari stateful menjadi stateless dengan menghilangkan semua atribut yang tidak diperlukan dan menggantinya dengan kode MyHomePage({Key? key}) : super(key: key);.
- Hapus fungsi State yang tidak lagi diperlukan.

4) Langkah 4: Menambahkan Teks dan Card

- Membuat kelas model ShopItem yang memiliki atribut name, icon, dan color.
- Membuat daftar item yang dijual dalam variabel items, yang berisi objek ShopItem dengan nama, ikon, dan warna.
- Mengganti isi dari widget build di dalam MyHomePage untuk menampilkan judul toko, membuat grid layout, dan menampilkan setiap item sebagai ShopCard.

5) Langkah 5: Membuat Widget ShopCard

- Membuat widget ShopCard sebagai widget stateless baru untuk menampilkan setiap item toko.
- Menggunakan widget Material untuk mengatur latar belakang dengan warna indigo.
- Menambahkan interaksi dengan menggunakan widget InkWell untuk menampilkan pesan SnackBar ketika item toko ditekan.
- Menampilkan ikon dan teks yang sesuai dengan item toko.


