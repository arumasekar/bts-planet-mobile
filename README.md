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

-------------------------------------------

# Tugas 8

1. Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat!

Perbedaan antara Navigator.push() dan Navigator.pushReplacement() adalah sebagai berikut:

- Navigator.push() adalah metode yang digunakan untuk berpindah ke route baru dengan menambahkan route tersebut ke tumpukan route yang dikelola oleh Navigator. Metode ini akan menampilkan animasi transisi yang sesuai dengan platform. Route yang sebelumnya tidak akan dihapus, tetapi hanya disembunyikan. Hal ini memungkinkan pengguna untuk kembali ke route sebelumnya dengan menggunakan tombol back atau Navigator.pop().

- Navigator.pushReplacement() adalah metode yang digunakan untuk berpindah ke route baru dengan menggantikan route saat ini dengan route baru. Metode ini juga akan menampilkan animasi transisi yang sesuai dengan platform. Route yang sebelumnya akan dihapus dari tumpukan route, sehingga pengguna tidak dapat kembali ke route sebelumnya dengan menggunakan tombol back atau Navigator.pop().

Contoh penggunaan kedua metode tersebut yang tepat adalah:

- Navigator.push(): Misalnya kita ingin membuat aplikasi yang memiliki dua halaman, yaitu halaman utama dan halaman detail. Pada halaman utama, kita menampilkan daftar produk yang dapat diklik oleh pengguna. Ketika pengguna mengklik salah satu produk, kita ingin menampilkan halaman detail yang berisi informasi lebih lanjut tentang produk tersebut. Kita bisa menggunakan Navigator.push() untuk berpindah ke halaman detail, dan memungkinkan pengguna untuk kembali ke halaman utama dengan menggunakan tombol back atau Navigator.pop(). 

Berikut adalah kode yang bisa kita gunakan:


```// Membuat widget untuk halaman utama
class HomePage extends StatelessWidget {
  const HomePage({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    // Membuat daftar produk contoh
    final products = [
      Product(name: 'Laptop', price: 10000000),
      Product(name: 'Smartphone', price: 5000000),
      Product(name: 'Headset', price: 200000),
    ];

    // Mengembalikan widget Scaffold yang berisi AppBar dan ListView
    return Scaffold(
      appBar: AppBar(
        title: const Text('Daftar Produk'),
      ),
      body: ListView.builder(
        itemCount: products.length,
        itemBuilder: (context, index) {
          // Membuat widget ListTile untuk setiap produk
          return ListTile(
            title: Text(products[index].name),
            subtitle: Text('Rp ${products[index].price}'),
            onTap: () {
              // Berpindah ke halaman detail dengan menggunakan Navigator.push()
              Navigator.push(
                context,
                MaterialPageRoute(
                  builder: (context) => DetailPage(product: products[index]),
                ),
              );
            },
          );
        },
      ),
    );
  }
}

// Membuat widget untuk halaman detail
class DetailPage extends StatelessWidget {
  // Menerima objek produk sebagai parameter
  final Product product;

  const DetailPage({Key? key, required this.product}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    // Mengembalikan widget Scaffold yang berisi AppBar dan Center
    return Scaffold(
      appBar: AppBar(
        title: const Text('Detail Produk'),
      ),
      body: Center(
        // Menampilkan nama dan harga produk
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text(product.name, style: const TextStyle(fontSize: 24)),
            const SizedBox(height: 16),
            Text('Rp ${product.price}', style: const TextStyle(fontSize: 18)),
          ],
        ),
      ),
    );
  }
}

// Membuat kelas untuk merepresentasikan produk
class Product {
  final String name;
  final int price;

  Product({required this.name, required this.price});
}
```

- Navigator.pushReplacement(): Misalnya kita ingin membuat aplikasi yang memiliki tiga halaman, yaitu halaman login, halaman utama, dan halaman profil. Pada halaman login, kita menampilkan form untuk memasukkan email dan password pengguna. Ketika pengguna berhasil login, kita ingin menampilkan halaman utama yang berisi menu untuk berpindah ke halaman profil. Kita bisa menggunakan Navigator.pushReplacement() untuk berpindah dari halaman login ke halaman utama, dan menghapus halaman login dari tumpukan route. Hal ini akan mencegah pengguna untuk kembali ke halaman login dengan menggunakan tombol back atau Navigator.pop(). Berikut adalah kode yang bisa kita gunakan:

```// Membuat widget untuk halaman login
class LoginPage extends StatelessWidget {
  const LoginPage({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    // Membuat controller untuk email dan password
    final emailController = TextEditingController();
    final passwordController = TextEditingController();

    // Mengembalikan widget Scaffold yang berisi AppBar dan Padding
    return Scaffold(
      appBar: AppBar(
        title: const Text('Halaman Login'),
      ),
      body: Padding(
        padding: const EdgeInsets.all(16),
        // Menampilkan form untuk email dan password
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            TextField(
              controller: emailController,
              decoration: const InputDecoration(
                labelText: 'Email',
                border: OutlineInputBorder(),
              ),
            ),
            const SizedBox(height: 16),
            TextField(
              controller: passwordController,
              obscureText: true,
              decoration: const InputDecoration(
                labelText: 'Password',
                border: OutlineInputBorder(),
              ),
            ),
            const SizedBox(height: 16),
            ElevatedButton(
              child: const Text('Login'),
              onPressed: () {
                // Mengecek apakah email dan password benar
                if (emailController.text == 'user@example.com' &&
                    passwordController.text == '123456') {
                  // Berpindah ke halaman utama dengan menggunakan Navigator.pushReplacement()
                  Navigator.pushReplacement(
                    context,
                    MaterialPageRoute(
                      builder: (context) => const HomePage(),
                    ),
                  );
                } else {
                  // Menampilkan pesan error
                  ScaffoldMessenger.of(context).showSnackBar(
                    const SnackBar(
                      content: Text('Email atau password salah'),
                    ),
                  );
                }
              },
            ),
          ],
        ),
      ),
    );
  }
}

// Membuat widget untuk halaman utama
class HomePage extends StatelessWidget {
  const HomePage({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    // Mengembalikan widget Scaffold yang berisi AppBar dan Center
    return Scaffold(
      appBar: AppBar(
        title: const Text('Halaman Utama'),
      ),
      body: Center(
        // Menampilkan menu untuk berpindah ke halaman profil
        child: ElevatedButton(
          child: const Text('Lihat Profil'),
          onPressed: () {
            // Berpindah ke halaman profil dengan menggunakan Navigator.push()
            Navigator.push(
              context,
              MaterialPageRoute(
                builder: (context) => const ProfilePage(),
              ),
            );
          },
        ),
      ),
    );
  }
}

// Membuat widget untuk halaman profil
class ProfilePage extends StatelessWidget {
  const ProfilePage({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    // Mengembalikan widget Scaffold yang berisi AppBar dan Center
    return Scaffold(
      appBar: AppBar(
        title: const Text('Halaman Profil'),
      ),
      body: Center(
        // Menampilkan nama dan email pengguna
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: const [
            Text('User', style: TextStyle(fontSize: 24)),
            SizedBox(height: 16),
            Text('user@example.com', style: TextStyle(fontSize: 18)),
          ],
        ),
      ),
    );
  }
}
```

Sumber:
- https://stackoverflow.com/questions/71609393/what-is-the-difference-between-navigator-pushreplacement-and-navigator-pushandre
- https://docs.flutter.dev/cookbook/navigation/navigation-basics
- https://davy.ai/what-is-the-difference-between-navigator-pushreplacement-and-navigator-pushandremoveuntil-in-flutter/
- https://stackoverflow.com/questions/71609113/flutter-what-is-the-difference-between-using-pushreplacementnamed-and-pushrep


2. Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing!

Berikut adalah penjelasan masing-masing layout widget pada Flutter dan konteks penggunaannya:

- Row: Row adalah widget yang menyusun anak-anaknya secara horizontal, yaitu sejajar dengan sumbu x. Row dapat digunakan untuk membuat layout yang membutuhkan elemen-elemen yang berdampingan, seperti menu, toolbar, atau tombol. Row memiliki beberapa properti yang dapat mengatur posisi, ukuran, dan jarak antara anak-anaknya, seperti mainAxisAlignment, crossAxisAlignment, mainAxisSize, dan children.

- Column: Column adalah widget yang menyusun anak-anaknya secara vertikal, yaitu sejajar dengan sumbu y. Column dapat digunakan untuk membuat layout yang membutuhkan elemen-elemen yang bertumpuk, seperti daftar, form, atau kartu. Column memiliki properti yang mirip dengan Row, seperti mainAxisAlignment, crossAxisAlignment, mainAxisSize, dan children.

- Wrap: Wrap adalah widget yang menyusun anak-anaknya secara horizontal atau vertikal, tetapi dapat menggulung ke baris atau kolom berikutnya jika tidak ada ruang yang cukup. Wrap dapat digunakan untuk membuat layout yang fleksibel dan responsif, seperti tag, chip, atau galeri. Wrap memiliki beberapa properti yang dapat mengatur arah, spasi, dan rungutan anak-anaknya, seperti direction, alignment, spacing, runAlignment, runSpacing, dan children.

- Center: Center adalah widget yang menempatkan anaknya di tengah-tengah dirinya sendiri. Center dapat digunakan untuk membuat layout yang membutuhkan elemen-elemen yang berada di posisi sentral, seperti judul, logo, atau gambar. Center memiliki satu properti yang dapat mengatur ukuran anaknya, yaitu child.

- Stack: Stack adalah widget yang menyusun anak-anaknya di atas satu sama lain, yaitu sejajar dengan sumbu z. Stack dapat digunakan untuk membuat layout yang membutuhkan elemen-elemen yang tumpang tindih, seperti latar belakang, overlay, atau animasi. Stack memiliki dua properti yang dapat mengatur posisi dan ukuran anak-anaknya, yaitu alignment dan children. Anak-anak Stack dapat menggunakan widget Positioned untuk menentukan posisi relatifnya terhadap Stack.

- Container: Container adalah widget yang dapat menggabungkan beberapa fungsi layout, seperti padding, margin, border, warna, ukuran, dan transformasi. Container dapat digunakan untuk membuat layout yang membutuhkan elemen-elemen yang memiliki dekorasi atau dimensi tertentu, seperti kotak, panel, atau bidang. Container memiliki beberapa properti yang dapat mengatur tampilan dan perilakunya, seperti padding, margin, decoration, color, width, height, alignment, transform, dan child.

Sumber:
- https://docs.flutter.dev/ui/widgets/layout
- https://www.petanikode.com/flutter-widget/#google_vignette
- https://www.bing.com/search?q=layout+widget+pada+Flutter&toWww=1&redig=4F6ECFC8FBAD4E7DB8A6AABBC9B6FBF4
- https://www.bing.com/search?q=layout+widget+pada+Flutter&toWww=1&redig=4F6ECFC8FBAD4E7DB8A6AABBC9B6FBF4
- https://jagongoding.com/android/flutter/layout-dasar/persiapan/


3. Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut!

- TextFormField untuk Nama Item:

Tujuan: Untuk memasukkan nama item yang akan ditambahkan.
Alasan Penggunaan: TextFormField cocok digunakan untuk input teks sederhana. Saya menggunakan validator untuk memastikan bahwa field tidak kosong, yang menunjukkan bahwa nama item adalah informasi penting yang harus diisi.

```
Padding(
  padding: const EdgeInsets.all(8),
  child: TextFormField(
    decoration: InputDecoration(
      hintText: "Nama Item",
      labelText: "Nama Item",
      border: OutlineInputBorder(
          borderRadius: BorderRadius.circular(5))),
    onChanged: (String? value) {
      setState(() {
        _name = value!;
      });
    },
    validator: (String? value) {
      if (value == null || value.isEmpty) {
        return "Nama Item Tidak Boleh Kosong!";
      }
      return null;
    },
  ),
),
```

- TextFormField untuk Jumlah Item:

Tujuan: Untuk memasukkan jumlah item dalam bentuk angka.
Alasan Penggunaan: Lagi-lagi TextFormField digunakan, tetapi kali ini untuk input numerik. Saya mengubah teks input menjadi integer dan memvalidasi untuk memastikan bahwa input adalah angka dan tidak kosong. Ini penting untuk memastikan bahwa jumlah item yang diinput valid.

```
Padding(
  padding: const EdgeInsets.all(8.0),
  child: TextFormField(
    decoration: InputDecoration(
      hintText: "Jumlah Item",
      labelText: "Jumlah Item",
      border: OutlineInputBorder(
        borderRadius: BorderRadius.circular(5.0),
      ),
    ),
    onChanged: (String? value) {
      setState(() {
        _amount = int.parse(value!);
      });
    },
    validator: (String? value) {
      if (value == null || value.isEmpty) {
        return "Jumlah Item Tidak Boleh kosong!";
      }
      if (int.tryParse(value) == null) {
        return "Jumlah Item Harus Bilangan!";
      }
      return null;
    },
  ),
),
```

- TextFormField untuk Deskripsi:

Tujuan: Untuk memasukkan deskripsi item.
Alasan Penggunaan: Seperti input nama item, TextFormField digunakan untuk input teks yang lebih panjang seperti deskripsi. Validator memastikan bahwa deskripsi tidak dibiarkan kosong, menunjukkan pentingnya informasi deskriptif untuk setiap item.

```
Padding(
  padding: const EdgeInsets.all(8.0),
  child: TextFormField(
    decoration: InputDecoration(
      hintText: "Deskripsi",
      labelText: "Deskripsi",
      border: OutlineInputBorder(
        borderRadius: BorderRadius.circular(5.0),
      ),
    ),
    onChanged: (String? value) {
      setState(() {
        _description = value!;
      });
    },
    validator: (String? value) {
      if (value == null || value.isEmpty) {
        return "Deskripsi Tidak Boleh Kosong!";
      }
      return null;
    },
  ),
),
```

4. Bagaimana penerapan clean architecture pada aplikasi Flutter?

Penerapan clean architecture pada aplikasi Flutter adalah salah satu cara untuk membuat aplikasi yang bersih, modular, dan mudah diuji. Clean architecture pada aplikasi Flutter biasanya terdiri dari tiga lapisan utama, yaitu:

- Lapisan presentasi (UI): Lapisan ini berisi komponen antarmuka pengguna, seperti widget, layar, dan tampilan. Lapisan ini bertanggung jawab untuk menangani interaksi pengguna dan menampilkan UI. Lapisan ini juga menggunakan berbagai pola manajemen state untuk mengontrol state dari widget.

- Lapisan domain (bisnis): Lapisan ini merepresentasikan logika bisnis inti dari aplikasi. Lapisan ini berisi entitas, use case, dan repository interface. Entitas adalah kelas yang merepresentasikan objek bisnis, seperti produk, pengguna, atau pesanan. Use case adalah kelas yang merepresentasikan fungsi bisnis, seperti login, daftar, atau beli. Repository interface adalah abstraksi dari sumber data, yang mendefinisikan kontrak untuk mengambil dan menyimpan data.

- Lapisan data: Lapisan ini bertanggung jawab untuk pengambilan dan penyimpanan data. Lapisan ini berisi implementasi dari repository interface, yang dapat berupa local data source (misalnya SQLite, Shared Preferences, atau Hive) atau remote data source (misalnya REST API, Firebase, atau GraphQL). Lapisan ini juga berisi model, yang adalah kelas yang merepresentasikan struktur data, seperti JSON, XML, atau Map¹².

Selain tiga lapisan utama, ada juga dua lapisan pendukung, yaitu:

- Lapisan resource: Lapisan ini berisi sumber daya yang digunakan oleh aplikasi, seperti string, warna, gambar, atau font. Lapisan ini memudahkan untuk mengelola dan mengubah sumber daya tanpa mengubah kode.
- Lapisan shared library: Lapisan ini berisi kelas-kelas yang digunakan oleh banyak lapisan lain, seperti konstanta, utilitas, ekstensi, atau widget kustom. Lapisan ini memudahkan untuk menghindari duplikasi kode dan meningkatkan modularitas.

Untuk menerapkan clean architecture pada aplikasi Flutter, kita dapat mengikuti langkah-langkah berikut:

- Membuat folder untuk setiap lapisan, seperti presentation, domain, data, resource, dan shared.
- Membuat folder untuk setiap fitur, seperti home, login, atau profile. Setiap folder fitur dapat memiliki subfolder untuk setiap lapisan, seperti pages, widgets, use_cases, entities, models, atau repositories.
- Membuat kelas-kelas yang sesuai dengan lapisan dan fitur yang dibutuhkan, seperti HomePage, LoginUseCase, UserEntity, UserModel, atau UserRepository.
- Menggunakan dependency injection untuk menyediakan ketergantungan kelas, seperti use case, repository, atau data source. Dependency injection dapat membantu untuk mengurangi kopling antara kelas dan memudahkan untuk pengujian.
- Menggunakan prinsip-prinsip pemrograman yang baik, seperti single responsibility, open-closed, atau dependency inversion. Prinsip-prinsip ini dapat membantu untuk membuat kode yang bersih, mudah dibaca, dan mudah dimodifikasi.

Sumber:
- https://medium.com/ruangguru/an-introduction-to-flutter-clean-architecture-ae00154001b0
- https://medium.com/@samra.sajjad0001/flutter-clean-architecture-5de5e9b8d093
- https://belajarinformatika.com/flutter-clean-architecture-template/
- https://flutterawesome.com/flutter-app-utilizando-clean-architecture/
- https://www.udemy.com/course/tutorial-flutter-371-clean-code-architecture-uncle-bob/


5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial)

- Pembuatan Widget Drawer: Pertama, buatlah sebuah berkas baru dengan nama left_drawer.dart dalam direktori widgets. Dalam berkas ini, buatlah kelas LeftDrawer yang mengembalikan widget Drawer. Isi Drawer ini akan berupa ListView yang berisi DrawerHeader dan beberapa item untuk navigasi.

```
import 'package:flutter/material.dart';

class LeftDrawer extends StatelessWidget {
  const LeftDrawer({super.key});

  @override
  Widget build(BuildContext context) {
    return Drawer(
      child: ListView(
        children: [
          const DrawerHeader(
            // Bagian header drawer
          ),
          // Bagian item navigasi
        ],
      ),
    );
  }
}
```

- Menambahkan Navigasi ke Drawer: Tambahkan navigasi ke halaman yang diinginkan. Misalnya, tambahkan navigasi ke MyHomePage dan ShopFormPage. Gunakan widget ListTile untuk setiap item navigasi dan gunakan metode Navigator.pushReplacement() untuk navigasi.

```
ListTile(
  leading: const Icon(Icons.home_outlined),
  title: const Text('Halaman Utama'),
  onTap: () {
    Navigator.pushReplacement(
        context,
        MaterialPageRoute(builder: (context) => MyHomePage()),
    );
  },
),
ListTile(
  leading: const Icon(Icons.add_shopping_cart),
  title: const Text('Tambah Produk'),
  onTap: () {
    // Navigasi ke ShopFormPage
  },
),
```

Menghias Drawer: Tambahkan desain pada DrawerHeader. Misalnya, gunakan warna, teks, dan styling untuk membuat header yang menarik.
```
const DrawerHeader(
  decoration: BoxDecoration(color: Colors.indigo),
  child: Column(
    children: [
      Text('Shopping List', style: TextStyle(/* Styling teks */)),
      // Konten tambahan
    ],
  ),
),
```

- Menyertakan Drawer di Halaman Utama: Setelah membuat LeftDrawer, sertakan sebagai parameter drawer di widget Scaffold pada halaman utama aplikasi.

```
return Scaffold(
  appBar: AppBar(title: const Text('Shopping List')),
  drawer: const LeftDrawer(),
  // Konten lain dari Scaffold
);
```

Selanjutnya, kita juga akan membuat form untuk memasukkan data barang menggunakan widget Form. Form ini akan berisi beberapa TextFormField untuk mengumpulkan informasi seperti nama, harga, dan deskripsi produk.

- Pembuatan Halaman Form: Buatlah halaman baru dengan nama shoplist_form.dart. Dalam halaman ini, buatlah kelas ShopFormPage yang mengembalikan widget Form di dalam Scaffold.

```
class ShopFormPage extends StatefulWidget {
  const ShopFormPage({super.key});

  @override
  State<ShopFormPage> createState() => _ShopFormPageState();
}

class _ShopFormPageState extends State<ShopFormPage> {
  final _formKey = GlobalKey<FormState>();
  String _name = "";
  int _price = 0;
  String _description = "";

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Form Tambah Produk')),
      body: Form(
        key: _formKey,
        child: SingleChildScrollView(
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: [
              // TextFormField untuk nama, harga, dan deskripsi
            ],
          ),
        ),
      ),
    );
  }
}
```

- Menambahkan Field Input: Untuk setiap field input seperti nama, harga, dan deskripsi, gunakan TextFormField yang dibungkus dalam Padding. Tambahkan validator untuk memastikan input valid.

```
Padding(
  padding: const EdgeInsets.all(8.0),
  child: TextFormField(
    // Konfigurasi untuk field nama
  ),
),
// Ulangi untuk field harga dan deskripsi
```

- Menambahkan Tombol Simpan: Tambahkan tombol yang akan menyimpan data ketika ditekan. Gunakan ElevatedButton di dalam Align dan Padding.

```
Align(
  alignment: Alignment.bottomCenter,
  child: Padding(
    padding: const EdgeInsets.all(8.0),
    child: ElevatedButton(
      onPressed: () {
        if (_formKey.currentState!.validate()) {
          // Tampilkan dialog atau lakukan aksi lain
        }
      },
      child: const Text('Simpan'),
    ),
  ),
),
```

- Menampilkan Data: Gunakan showDialog() untuk menampilkan informasi yang telah disimpan saat tombol ditekan.

```
showDialog(
  context: context,
  builder: (context) {
    return AlertDialog(
      title: const Text('Produk berhasil tersimpan'),
      content: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          Text('Nama: $_name'),
          // Tampilkan informasi lain
        ],
      ),
    );
  },
);
```

Terakhir, tambahkan fitur navigasi pada tombol di halaman utama untuk memungkinkan pengguna berpindah ke halaman form yang baru dibuat. Gunakan Navigator.push() untuk melakukan ini.

-------------------------------------------

# Tugas 9

1. Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?
Tentu, kita dapat mengambil data dari JSON tanpa perlu membuat model terlebih dahulu. Ada beberapa cara untuk melakukannya. Salah satunya adalah menggunakan metode JObject.Parse(), yang memungkinkan kita untuk mengonversi string JSON menjadi objek JObject dan mengakses nilai-nilai yang dibutuhkan. Alternatif lainnya adalah menggunakan pustaka Json.NET untuk melakukan serialisasi dan deserialisasi objek JSON, atau dengan mendeserialisasi JSON ke dalam objek dinamis, atau menggunakan metode JsonValue.Parse() untuk mengurai teks JSON dan mendapatkan nilai dari JsonValue.

Sumber:
- https://stackoverflow.com/questions/75638056/how-to-parse-json-data-without-model-class-in-flutter-and-get-single-value
- https://stackoverflow.com/questions/68343117/json-request-without-model-binding-in-asp-net-core-webapi

2.  Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
CookieRequest adalah sebuah kelas dalam aplikasi Flutter yang berguna untuk mengirim permintaan HTTP sambil memanfaatkan cookie yang tersimpan di CookieJar. Kelas ini memungkinkan untuk melakukan berbagai jenis permintaan HTTP, seperti GET, POST, PUT, DELETE, atau PATCH, dengan otomatis menambahkan header Cookie yang sesuai dengan URL yang dituju. Selain itu, CookieRequest juga memiliki kemampuan untuk menerima dan menyimpan cookie yang dikirim oleh server sebagai header Set-Cookie¹.

Pentingnya berbagi instance CookieRequest ke semua komponen dalam aplikasi Flutter dapat dijelaskan oleh alasan berikut:
- CookieRequest memungkinkan aplikasi Flutter untuk berinteraksi dengan server yang mengharuskan autentikasi atau menggunakan sesi berbasis cookie, seperti proses login, logout, atau mengakses data pribadi pengguna.
- Dengan CookieRequest, manajemen cookie yang diperlukan oleh aplikasi Flutter menjadi lebih mudah, termasuk operasi seperti menyimpan, memuat, menghapus, atau memperbarui cookie secara otomatis.
- Penggunaan CookieRequest dapat meningkatkan kinerja aplikasi Flutter dengan mengurangi jumlah permintaan yang harus dikirim ke server, sekaligus melindungi cookie dari potensi akses yang tidak sah atau serangan man-in-the-middle.

Dengan kata lain, berbagi instance CookieRequest di seluruh komponen aplikasi Flutter membantu menjaga otentikasi, mengelola cookie secara efisien, dan meningkatkan tingkat keamanan dan performa keseluruhan aplikasi.

Sumber:
- https://codewithflutter.com/how-do-i-make-an-http-request-using-cookies-on-flutter/
- https://learnpainless.com/how-set-cookie-header-with-request-flutter/
- https://stackoverflow.com/questions/52500575/post-request-with-cookies-in-flutter
- https://api.flutter.dev/flutter/dart-io/Cookie-class.html

3.  Jelaskan mekanisme pengambilan data dari JSON hingga dapat ditampilkan pada Flutter.
Untuk mengambil data dari JSON dan menampilkannya di Flutter, beberapa langkah yang perlu diikuti adalah sebagai berikut:
- Membuat model data yang sesuai dengan struktur JSON yang akan diambil. Model data adalah kelas yang mendefinisikan properti dan metode terkait dengan data yang akan digunakan. Model data berguna untuk memvalidasi, memanipulasi, dan mentransformasi data dengan lebih mudah dan aman.
- Menggunakan paket atau plugin yang mendukung pengiriman permintaan HTTP ke API yang menyediakan data JSON, seperti http, dio, chopper, dll. Paket atau plugin ini mempermudah pengaturan parameter, header, body, dan respon dari permintaan HTTP yang dikirim.
- Menggunakan fungsi atau metode untuk mengurai atau mendeserialisasi data JSON yang diterima dari API menjadi objek Dart. Fungsi atau metode ini membantu mengonversi data JSON menjadi objek model data yang telah dibuat sebelumnya.
- Menggunakan widget atau komponen dalam Flutter untuk menampilkan data JSON yang telah diubah menjadi objek Dart. Contoh widget yang berguna termasuk ListView, ListTile, Card, Text, Image, dan lainnya. Widget ini memungkinkan pembuatan tampilan yang menarik dan interaktif untuk data JSON yang akan ditampilkan.
Di bawah ini adalah contoh kode yang menunjukkan bagaimana langkah-langkah ini dapat diterapkan dengan Flutter, dengan menggunakan paket http dan model data Character:

```
// Import paket yang diperlukan
import 'package:flutter/material.dart';
import 'package:http/http.dart' as http;
import 'dart:convert';

// Membuat model data Character
class Character {
  final int id;
  final String name;
  final String image;
  final String status;

  Character({
    required this.id,
    required this.name,
    required this.image,
    required this.status,
  });

  factory Character.fromJson(Map<String, dynamic> json) {
    return Character(
      id: json['id'],
      name: json['name'],
      image: json['image'],
      status: json['status'],
    );
  }
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'JSON Example',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: MyHomePage(),
    );
  }
}

class MyHomePage extends StatefulWidget {
  @override
  _MyHomePageState createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  List<Character> characters = [];

  Future<void> fetchCharacters() async {
    final response = await http.get(Uri.parse('https://rickandmortyapi.com/api/character'));

    if (response.statusCode == 200) {
      final result = jsonDecode(response.body);
      Iterable list = result['results'];

      setState(() {
        characters = list.map((character) => Character.fromJson(character)).toList();
      });
    } else {
      print('Request failed with status: ${response.statusCode}.');
    }
  }

  Widget characterList() {
    return ListView.builder(
      itemCount: characters.length,
      itemBuilder: (context, index) {
        return Card(
          child: ListTile(
            leading: Image.network(characters[index].image),
            title: Text(characters[index].name),
            subtitle: Text(characters[index].status),
          ),
        );
      },
    );
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('JSON Example'),
      ),
      body: characterList(),
      floatingActionButton: FloatingActionButton(
        child: Icon(Icons.refresh),
        onPressed: fetchCharacters,
      ),
    );
  }
}

void main() {
  runApp(MyApp());
}
```

4.  Jelaskan mekanisme autentikasi dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.
Berikut adalah mekanisme autentikasi input data akun dari Flutter ke Django hingga penyelesaian proses autentikasi oleh Django dan tampilnya menu pada Flutter dalam bentuk parafrase:
- Awalnya, pengguna memasukkan informasi akun, seperti username dan password, menggunakan widget TextField atau TextFormField di dalam aplikasi Flutter. Data akun ini kemudian disimpan dalam variabel atau controller yang dapat digunakan untuk melakukan permintaan HTTP.
- Selanjutnya, Flutter mengirimkan permintaan HTTP POST ke API Django yang bertanggung jawab untuk menghasilkan token autentikasi, biasanya melalui URL seperti `http://IP:8000/get-token/`. Permintaan ini mencakup data akun pengguna sebagai bagian dari tubuh permintaan (body), serta header yang mengindikasikan jenis konten dan penerimaan data, seperti `{"Content-Type": "application/json", "Accept": "application/json"}`.
- Setelah itu, Django menerima permintaan HTTP POST dari Flutter dan melakukan validasi terhadap data akun pengguna menggunakan modul autentikasi yang telah disediakan oleh Django. Jika data akun valid, Django akan menghasilkan token autentikasi dengan menggunakan paket atau plugin yang dapat mengelola token, seperti django-rest-framework-simplejwt, django-rest-framework-jwt, atau django-rest-knox. Token autentikasi ini kemudian dikirimkan kembali ke Flutter sebagai respons HTTP dalam format JSON, seperti `{"access": "nilai_token"}`.
- Selanjutnya, Flutter menerima respons HTTP dari Django dan melakukan parsing atau deserialisasi data JSON yang berisi token autentikasi. Token autentikasi ini kemudian disimpan oleh Flutter dalam penyimpanan lokal atau aman, seperti SharedPreferences atau FlutterSecureStorage. Token ini akan digunakan untuk mengakses API Django yang memerlukan autentikasi, misalnya, `http://IP:8000/database/exercises/`.
- Terakhir, berdasarkan status autentikasi pengguna, Flutter akan menampilkan menu atau halaman yang sesuai. Jika pengguna berhasil masuk, Flutter akan menampilkan menu atau halaman yang berisi berbagai fitur yang dapat digunakan pengguna, seperti melihat, menambah, mengedit, atau menghapus data. Namun, jika pengguna gagal masuk, Flutter dapat menampilkan pesan kesalahan atau mengarahkan kembali ke halaman login.

Sumber:
- https://dev.to/amartyadev/flutter-app-authentication-with-django-backend-1-21cp
- https://stackoverflow.com/questions/56366828/authenticate-user-in-django-via-flutter-app-and-json-web-token
- https://stackoverflow.com/questions/74383879/how-to-add-user-token-from-flutter-to-django-rest-framework-to-avoid-forbidden-a
- https://docs.flutter.dev/cookbook/networking/authenticated-requests

5.  Sebutkan seluruh widget yang kamu pakai pada tugas ini dan jelaskan fungsinya masing-masing.
Pada tugas yang kita berikan, beberapa widget Flutter yang digunakan termasuk:
- `MaterialApp`: Widget ini digunakan untuk menginisialisasi dan mengatur tema serta konfigurasi dasar aplikasi Flutter.
- `Scaffold`: Digunakan untuk membuat tampilan dasar aplikasi, termasuk AppBar dan body.
- `AppBar`: Menampilkan app bar di atas layar dengan judul yang sesuai.
- `Drawer`: Membuat menu navigasi samping (drawer) yang dapat diakses dengan menggeser dari kiri ke kanan.
- `TextField`: Digunakan untuk membuat input teks untuk username dan password pada halaman login.
- `ElevatedButton`: Tombol yang digunakan untuk mengirim data login ke server Django.
- `FutureBuilder`: Menggunakan Future untuk mengambil data dari web service Django dan menampilkan hasilnya pada tampilan aplikasi.
- `ListView.builder`: Digunakan untuk menampilkan daftar produk yang diterima dari server dalam bentuk daftar scrollable.
- `Text`: Untuk menampilkan teks pada tampilan aplikasi.
- `AlertDialog`: Digunakan untuk menampilkan dialog pada aplikasi.
- `SnackBar`: Untuk menampilkan pesan sementara yang muncul di bagian bawah layar.
- `Icon`: Menampilkan ikon seperti ikon keranjang belanja pada menu.
- `DrawerHeader`: Bagian header dari drawer yang berisi judul atau informasi tambahan.
- `ListTile`: Digunakan untuk membuat item daftar pada drawer.
- `Navigator`: Untuk melakukan navigasi antara halaman-halaman aplikasi.
- `Provider`: Digunakan untuk manajemen state dalam aplikasi dan membagikan instance `CookieRequest` ke komponen-komponen yang membutuhkannya.
- Beberapa widget lain seperti `Container`, `Column`, `Row`, dan `SizedBox` digunakan untuk mengatur tata letak dan penampilan tampilan aplikasi.

6.  Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).

**Langkah 1: Menambahkan Dependensi HTTP**

Pada langkah ini, kita perlu menambahkan dependensi http ke proyek Flutter kita dengan menjalankan perintah berikut di terminal:

```
flutter pub add http
```

Ini akan menambahkan package http ke proyek kita, yang diperlukan untuk melakukan permintaan HTTP ke server Django.

**Langkah 2: Mengaktifkan Akses Internet di AndroidManifest.xml**

kita perlu memastikan bahwa aplikasi Flutter kita memiliki izin untuk mengakses internet. Untuk melakukan ini, tambahkan izin INTERNET di dalam file AndroidManifest.xml yang berada di dalam folder android/app/src/main/:

```xml
<uses-permission android:name="android.permission.INTERNET" />
```

**Langkah 3: Membuat View Django untuk Login**

Pada langkah ini, kita perlu membuat view Django yang akan digunakan untuk login. kita dapat membuatnya di views.py aplikasi Django kita. Pastikan view tersebut dapat menghandle permintaan POST yang berisi username dan password, dan memberikan respons JSON yang sesuai.

**Langkah 4: Menghubungkan Flutter dengan CookieRequest**

kita perlu menghubungkan halaman login Flutter dengan `CookieRequest` yang digunakan untuk mengirim permintaan HTTP ke server Django. kita dapat melakukannya dengan menambahkan baris berikut di dalam widget build pada halaman login Flutter:

```dart
final request = context.watch<CookieRequest>();
```

**Langkah 5: Mengimplementasikan Permintaan HTTP untuk Login**

kita perlu mengimplementasikan permintaan HTTP POST untuk login di halaman login Flutter. Ini biasanya dilakukan pada saat tombol login ditekan. kita dapat menggunakan package http untuk mengirim data login ke server Django dan menangani responsnya.

**Langkah 6: Menambahkan Respons Handling**

Setelah kita mengirim permintaan login ke server Django, kita perlu menangani respons yang diterima. Jika login berhasil, kita dapat melakukan navigasi ke halaman lain atau menampilkan pesan sukses. Jika login gagal, kita dapat menampilkan pesan kesalahan.

**Langkah 7: Membuat View Django untuk Logout**

Pada langkah ini, kita perlu membuat view Django yang akan digunakan untuk logout. Seperti pada langkah 3, pastikan view tersebut dapat menghandle permintaan POST dan memberikan respons JSON yang sesuai.

**Langkah 8: Menghubungkan Flutter dengan CookieRequest untuk Logout**

kita perlu menghubungkan widget yang akan melakukan logout di Flutter dengan `CookieRequest` yang digunakan untuk mengirim permintaan logout ke server Django.

**Langkah 9: Mengimplementasikan Permintaan HTTP untuk Logout**

Pada langkah ini, kita perlu mengimplementasikan permintaan HTTP POST untuk logout di Flutter. Ini biasanya dilakukan pada saat tombol logout ditekan. kita dapat menggunakan package http untuk mengirim permintaan logout ke server Django dan menangani responsnya.

**Langkah 10: Menambahkan Respons Handling untuk Logout**

Setelah kita mengirim permintaan logout ke server Django, kita perlu menangani respons yang diterima. Jika logout berhasil, kita dapat melakukan navigasi ke halaman login atau menampilkan pesan sukses. Jika logout gagal, kita dapat menampilkan pesan kesalahan.

Setelah mengikuti langkah-langkah di atas, kita akan memiliki implementasi login dan logout di aplikasi Flutter kita yang terhubung dengan server Django. Pastikan kita melakukan penyesuaian sesuai dengan kebutuhan aplikasi kita dan memastikan semua impor dan dependensi dikelola dengan baik.