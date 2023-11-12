# stock_mobile

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.


Tugas 7
1. 
   - Stateless Widget:
   Widget yang digunakan: StatelessWidget
   Fungsinya: Stateless widget adalah widget yang tidak dapat mengubah keadaannya setelah dibuat. Mereka berguna untuk bagian dari antarmuka pengguna yang tidak perlu mengubah tampilan atau data berdasarkan perubahan yang terjadi. Stateless widget ideal untuk komponen yang hanya perlu dirender satu kali dan tidak memiliki keadaan (state) yang berubah.

   - Stateful Widget:
   Widget yang digunakan: StatefulWidget
   Fungsinya: Stateful widget adalah widget yang mampu menyimpan dan mengelola keadaan (state) selama siklus hidupnya. Mereka berguna ketika Anda
   memiliki komponen yang perlu merespons perubahan data atau interaksi pengguna. Ketika keadaan di dalam stateful widget berubah, Flutter akan
   membangun ulang widget tersebut untuk mencerminkan perubahan tersebut.

2. 
   - MyHomePage (StatelessWidget):
   1. Scaffold: Ini adalah kerangka utama yang digunakan untuk mengatur tata letak halaman. Ini menyediakan appBar, body, dan sebagainya.
   2. AppBar: Ini adalah bilah atas yang menampilkan judul aplikasi dan mungkin beberapa ikon atau aksi.
   3. Text: Digunakan untuk menampilkan judul "Stock Mobile" di dalam AppBar.
   4. SingleChildScrollView: Digunakan untuk mengelilingi isi halaman. Ini memungkinkan kontennya dapat digulir jika kontennya terlalu panjang
   5. Padding: Ini digunakan untuk memberi jarak antara elemen-elemen dalam halaman.
   6. Column: Digunakan untuk menampilkan anak-anak secara vertikal, seperti judul, GridView, dan lainnya.
   7. GridView.count: Menampilkan daftar item toko dalam grid dengan jumlah kolom yang ditentukan.

   - ShopCard (StatelessWidget): 
   1. Material: Ini adalah elemen yang mengelilingi setiap item toko. Ini memberikan latar belakang berwarna biru muda.
   2. InkWell: Ini digunakan untuk membuat area yang responsif terhadap sentuhan sehingga ketika di-tap, akan muncul Snackbar.
   3. SnackBar: Muncul ketika item toko di-tap dan memberikan pesan yang sesuai.
   4. Container: Ini adalah wadah yang berisi ikon dan teks untuk setiap item toko.
   4. Icon: Menampilkan ikon yang mewakili item toko.
   5. Text: Menampilkan nama item toko. 

3. 
   1. Membuat Proyek Flutter Baru:
   buat proyek Flutter baru dengan nama "stock_mobile"

   2. Mengatur Struktur Proyek:
   atur ulang struktur file proyek dengan membuat file menu.dart dan memindahkan kode yang sesuai ke dalamnya. Selanjutnya, impor file tersebut ke dalam main.dart agar proyek berjalan dengan baik.
   
   3. Mengubah Tema Warna Aplikasi:
   ubah tema warna aplikasi sesuai keinginan dengan mengatur colorScheme pada main.dart.
   
   4. Mengubah Widget Menu Menjadi Stateless:
   
   5. Menambahkan Item Barang yang Dijual:
   definisikan tipe data ShopItem yang berisi informasi tentang barang yang dijual, seperti nama dan ikon.
   tambahkan daftar barang yang dijual ke dalam daftar items.

   6. Menampilkan Teks dan Cart Produk:
   tambahkan tampilan judul toko, menggunakan widget Text pada halaman.
   tampilkan daftar barang yang dijual dalam bentuk kartu dengan menggunakan widget ShopCard. Setiap kartu memiliki latar belakang yang berbeda dan menampilkan ikon dan nama barang.
   Ketika pengguna mengetuk salah satu kartu, muncul Snackbar yang memberikan pemberitahuan sesuai dengan barang yang dipilih.


Tugas 8

1. Perbedaan antara Navigator.push() dan Navigator.pushReplacement():

- Navigator.push(): Metode ini digunakan untuk menambahkan rute baru ke tumpukan navigasi tanpa menggantikan rute yang ada. Ini berarti rute sebelumnya tetap ada dalam tumpukan navigasi dan dapat dikembalikan ke belakang.
```dart
   Navigator.push(
   context,
   MaterialPageRoute(builder: (context) => SecondScreen()),
   );
```

- Navigator.pushReplacement(): Metode ini digunakan untuk menambahkan rute baru dan menggantikan rute saat ini dalam tumpukan navigasi. Ini bermanfaat ketika Anda ingin mengganti tampilan saat ini dengan tampilan baru dan tidak ingin kembali ke tampilan sebelumnya.
```dart
   Navigator.pushReplacement(
   context,
   MaterialPageRoute(builder: (context) => NewScreen()),
   );
```

2. - Container: Digunakan untuk mengelompokkan dan menata widget lain. Berguna untuk memberikan padding, margin, dan konfigurasi tata letak sederhana.
- Column dan Row: Digunakan untuk menata widget secara vertikal (Column) atau horizontal (Row). Berguna untuk menyusun widget secara berurutan.
- ListView: Digunakan untuk menampilkan daftar elemen yang dapat digulir. Berguna ketika Anda memiliki daftar item yang panjang.
- GridView: Menyusun widget dalam bentuk grid. Berguna untuk menampilkan elemen dalam tata letak berkolom dan berbaris.
- Stack: Menumpuk widget satu di atas yang lain. Berguna untuk menggabungkan widget secara bebas di atas satu sama lain.

3. - TextFormField untuk Nama Produk:
Digunakan untuk memasukkan nama produk.
Alasan Penggunaan: Untuk mendapatkan informasi tentang nama produk yang akan ditambahkan, dan sebagai validasi, tidak boleh kosong.

- TextFormField untuk Harga:
Digunakan untuk memasukkan harga produk.
Alasan Penggunaan: Untuk mendapatkan informasi tentang harga produk yang akan ditambahkan. Menerapkan validasi agar tidak boleh kosong dan harus berupa angka.

- TextFormField untuk Deskripsi:
Digunakan untuk memasukkan deskripsi produk.
Alasan Penggunaan: Untuk mendapatkan deskripsi produk yang akan ditambahkan, dan sebagai validasi, tidak boleh kosong.

Penjelasan
- TextFormField digunakan karena dapat menerima input teks dari pengguna.
- hintText dan labelText digunakan untuk memberikan petunjuk kepada pengguna mengenai informasi yang diharapkan pada setiap kolom input.
- onChanged digunakan untuk menangkap perubahan pada input dan mengubah nilai variabel yang sesuai.
- validator digunakan untuk memberikan validasi terhadap input yang diberikan oleh pengguna. Pesan kesalahan akan ditampilkan jika input tidak memenuhi kriteria yang ditentukan.

4. Penerapan Clean Architecture pada Aplikasi Flutter:
Pada kode yang diberikan, tidak ada implementasi secara eksplisit dari Clean Architecture. Clean Architecture menyarankan pemisahan kode menjadi beberapa lapisan untuk menjaga ketergantungan yang rendah dan memudahkan pengujian. Namun, di dalam kode tersebut, lapisan aplikasi tidak terpisah dengan jelas menjadi domain, data, dan presentasi. Implementasi yang lebih jelas dari Clean Architecture akan melibatkan struktur direktori yang terorganisir dan pemisahan tanggung jawab di antara lapisan-lapisan tersebut.


- Domain Layer:
Menyimpan logika dan inti aplikasi.

- Data Layer:
Menangani akses ke sumber data eksternal seperti database atau API.
Menyediakan repositori yang diimplementasikan di lapisan presentasi.

- Presentation Layer:
Menangani tampilan dan interaksi pengguna.
Menggunakan BLoC (Business Logic Component) untuk mengelola logika bisnis.
Menggunakan widget stateless atau stateful dan BLoC builder untuk memisahkan kode tampilan dari logika bisnis.

- Repository:
Merepresentasikan kontrak antara domain dan data layer.
Diimplementasikan di data layer untuk mengambil dan menyimpan data.


5. - Buat berkas left_drawer.dart:
Buat berkas baru di dalam direktori widgets dengan nama left_drawer.dart. 
```dart
import 'package:flutter/material.dart';

class LeftDrawer extends StatelessWidget {
  const LeftDrawer({Key? key});

  @override
  Widget build(BuildContext context) {
    return Drawer(
      child: ListView(
        children: [
          const DrawerHeader(
            // TODO: Bagian drawer header
          ),
          // TODO: Bagian routing
        ],
      ),
    );
  }
}
```

- Tambahkan Impor dan Routing pada left_drawer.dart:
```dart
import 'package:flutter/material.dart';
import 'package:shopping_list/menu.dart';
import 'package:shopping_list/shoplist_form.dart'; // TODO: Impor halaman ShopFormPage jika sudah dibuat
```

- Kemudian, tambahkan routing untuk MyHomePage dan ShopFormPage pada bagian routing
```dart
ListTile(
  leading: const Icon(Icons.home_outlined),
  title: const Text('Halaman Utama'),
  onTap: () {
    Navigator.pushReplacement(
      context,
      MaterialPageRoute(
        builder: (context) => MyHomePage(),
      ),
    );
  },
),
ListTile(
  leading: const Icon(Icons.add_shopping_cart),
  title: const Text('Tambah Produk'),
  onTap: () {
    Navigator.push(
      context,
      MaterialPageRoute(
        builder: (context) => ShopFormPage(),
      ),
    );
  },
),
```

- Hias Drawer dengan Drawer Header:
```dart
const DrawerHeader(
  decoration: BoxDecoration(
    color: Colors.indigo,
  ),
  child: Column(
    children: [
      Text(
        'Shopping List',
        textAlign: TextAlign.center,
        style: TextStyle(
          fontSize: 30,
          fontWeight: FontWeight.bold,
          color: Colors.white,
        ),
      ),
      Padding(
        padding: EdgeInsets.all(10),
      ),
      Text(
        "Catat seluruh keperluan belanjamu di sini!",
        style: TextStyle(
          textAlign: TextAlign.center,
          fontSize: 15,
          color: Colors.white,
          fontWeight: FontWeight.normal,
        ),
      ),
    ],
  ),
),
```

- Tambahkan Drawer ke Halaman Utama:
```dart
return Scaffold(
  appBar: AppBar(
    title: const Text(
      'Shopping List',
    ),
    backgroundColor: Colors.indigo,
    foregroundColor: Colors.white,
  ),
  drawer: const LeftDrawer(),
  // ... konten halaman utama
);
```

- Buat Halaman shoplist_form.dart
```dart
import 'package:flutter/material.dart';

class ShopFormPage extends StatefulWidget {
  const ShopFormPage({Key? key});

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
      appBar: AppBar(
        title: const Center(
          child: Text(
            'Form Tambah Produk',
          ),
        ),
        backgroundColor: Colors.indigo,
        foregroundColor: Colors.white,
      ),
      drawer: const LeftDrawer(),
      body: Form(
        key: _formKey,
        child: SingleChildScrollView(
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: [
              // ... Elemen input lainnya
            ],
          ),
        ),
      ),
    );
  }
}
```

- Isi Form dengan Elemen Input:
```dart
Padding(
  padding: const EdgeInsets.all(8.0),
  child: TextFormField(
    decoration: InputDecoration(
      hintText: "Nama Produk",
      labelText: "Nama Produk",
      border: OutlineInputBorder(
        borderRadius: BorderRadius.circular(5.0),
      ),
    ),
    onChanged: (String? value) {
      setState(() {
        _name = value!;
      });
    },
    validator: (String? value) {
      if (value == null || value.isEmpty) {
        return "Nama tidak boleh kosong!";
      }
      return null;
    },
  ),
),
Padding(
  padding: const EdgeInsets.all(8.0),
  child: TextFormField(
    decoration: InputDecoration(
      hintText: "Harga",
      labelText: "Harga",
      border: OutlineInputBorder(
        borderRadius: BorderRadius.circular(5.0),
      ),
    ),
    onChanged: (String? value) {
      setState(() {
        _price = int.parse(value!);
      });
    },
    validator: (String? value) {
      if (value == null || value.isEmpty) {
        return "Harga tidak boleh kosong!";
      }
      if (int.tryParse(value) == null) {
        return "Harga harus berupa angka!";
      }
      return null;
    },
  ),
),
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
        return "Deskripsi tidak boleh kosong!";
      }
      return null;
    },
  ),
),

```

- Tambahkan Tombol "Save"
```dart
Align(
  alignment: Alignment.bottomCenter,
  child: Padding(
    padding: const EdgeInsets.all(8.0),
    child: ElevatedButton(
      style: ButtonStyle(
        backgroundColor: MaterialStateProperty.all(Colors.indigo),
      ),
      onPressed: () {
        if (_formKey.currentState!.validate()) {
          showDialog(
            context: context,
            builder: (context) {
              return AlertDialog(
                title: const Text('Produk berhasil tersimpan'),
                content: SingleChildScrollView(
                  child: Column(
                    crossAxisAlignment: CrossAxisAlignment.start,
                    children: [
                      Text('Nama: $_name'),
                      Text('Harga: $_price'),
                      Text('Deskripsi: $_description'),
                    ],
                  ),
                ),
                actions: [
                  TextButton(
                    child: const Text('OK'),
                    onPressed: () {
                      Navigator.pop(context);
                    },
                  ),
                ],
              );
            },
          );
          _formKey.currentState!.reset();
        }
      },
      child: const Text(
        "Save",
        style: TextStyle(color: Colors.white),
      ),
    ),
  ),
),
```

- Tambahkan Fitur Navigasi pada Tombol:
```dart
onTap: () {
  ScaffoldMessenger.of(context)
    ..hideCurrentSnackBar()
    ..showSnackBar(SnackBar(
      content: Text("Kamu telah menekan tombol ${item.name}!")));

  if (item.name == "Tambah Produk") {
    Navigator.push(
      context,
      MaterialPageRoute(
        builder: (context) => ShopFormPage(),
      ),
    );
  }
},
```