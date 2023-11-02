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