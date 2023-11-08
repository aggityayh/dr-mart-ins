--- START TUGAS 7 ---

1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?
Pertama, StatelessWidget adalah jenis widget dalam Flutter yang tidak mengubah statenya setelah dibuat. Widget ini tetap sederhana dan cepat karena tidak ada manajemen state, sehingga pembuatan ulang widget berlangsung dengan sangat cepat. StatelessWidget cocok digunakan untuk bagian UI yang sederhana dan statis, seperti ikon, teks, dan gambar. Sedangkan, StatefulWidget, di sisi lain, dapat mengubah statenya sepanjang masa hidupnya. Ini memungkinkan widget untuk memperbarui UI berdasarkan interaksi pengguna atau data eksternal. Namun, StatefulWidget lebih kompleks karena memerlukan manajemen state yang rumit. Widget ini memelihara objek state terpisah yang menyimpan informasi state, bahkan saat terjadi hot reload atau pembuatan ulang widget. StatefulWidget cocok digunakan untuk bagian UI yang memerlukan interaksi pengguna atau pembaruan data, seperti formulir, animasi, atau timer.

2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.
- MyHomePage adalah kelas yang mewakili halaman utama dalam aplikasi Flutter. Kelas ini merupakan turunan dari StatelessWidget, yang berarti tidak menyimpan state antar pemanggilan build.

- Scaffold adalah widget yang menyediakan kerangka dasar tampilan visual untuk aplikasi. Ini mencakup elemen-elemen seperti AppBar, body (konten utama), dan floatingActionButton.

- AppBar adalah bagian dari desain Material yang digunakan untuk menampilkan judul aplikasi, branding, atau navigasi.

- Text adalah widget yang menampilkan teks dengan gaya yang dapat disesuaikan.

- SingleChildScrollView adalah sebuah box yang dapat di-scroll, cocok untuk kontainer tunggal dengan banyak anak tetapi tidak semuanya terlihat sekaligus.

- Padding adalah widget yang memberikan ruang kosong (padding) pada widget anaknya.

- Column adalah sebuah box yang menampilkan anak-anaknya dalam urutan vertikal.

- GridView adalah grid yang dapat di-scroll yang menampilkan widget sebagai tile (kotak kecil).

- ShopCard adalah kelas widget buatan sendiri yang menerima objek ShopItem dan menampilkan informasinya dalam bentuk kartu.

- Material adalah sebuah widget yang memberikan tampilan berdasarkan desain Material.

- InkWell adalah area berbentuk persegi panjang yang dapat diklik dan memberikan efek visual saat ditekan.

- Container adalah sebuah box yang berisi widget lain dan dapat diatur untuk memberikan padding, margin, ukuran, dan lain-lain.

- Icon adalah widget yang menampilkan ikon berdasarkan desain Material.

- Center adalah sebuah widget yang menengahkan widget anaknya di tengah-tengah tata letak.

3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)
- Membuat sebuah program Flutter baru dengan tema inventory seperti tugas-tugas sebelumnya.
Jalankan command flutter create mart_project untuk generate proyek Flutter
Masuk ke dalam direktori proyek tersebut dengan command cd mart_project

- Membuat Tiga Tombol Sederhana.
Buka file main.dart yang terletak di direktori lib pada proyek saya.
Tambahkan Tombol Pertama:

Dalam widget MyHomePage, tambahkan ElevatedButton pertama dengan ikon dan teks "Lihat Item".
Tambahkan Tombol Kedua dan Ketiga:

Selanjutnya, tambahkan ElevatedButton kedua dan ketiga dengan ikon dan teks "Tambah Item" dan "Logout" seperti yang telah dijelaskan sebelumnya.
Definisikan Aksi Tombol. Di dalam properti onPressed masing-masing tombol, saya dapat menentukan aksi yang akan dilakukan saat tombol ditekan. Namun, pada tahap ini, kita akan fokus pada menampilkan Snackbar.

- Menampilkan Snackbar.
Import Snackbar, saya telah mengimpor widget SnackBar di bagian atas file main.dart
import 'package:flutter/material.dart';
Gunakan ScaffoldMessenger:
Di dalam properti onPressed masing-masing tombol, gunakan ScaffoldMessenger.of(context).showSnackBar() untuk menampilkan Snackbar.

Contoh:
ScaffoldMessenger.of(context).showSnackBar(
  SnackBar(
    content: Text('Kamu telah menekan tombol Lihat Item'),
  ),
);

Ulangi langkah di atas untuk tombol "Tambah Item" dan "Logout", sesuaikan pesan Snackbar sesuai tombol yang ditekan.

- Menjalankan Aplikasi:
Simpan perubahan pada file main.dart dan jalankan aplikasi dengan perintah flutter run.

Ketika saya menjalankan aplikasi, saya akan melihat tiga tombol. Ketika saya menekan salah satu tombol, Snackbar akan muncul dengan pesan yang sesuai.

Pastikan bahwa setiap tombol memunculkan Snackbar dengan pesan yang benar saat ditekan.
Sekarang, saya seharusnya memiliki aplikasi Flutter dengan tiga tombol sederhana yang muncul Snackbar dengan pesan yang sesuai ketika ditekan. Jika ada masalah atau pertanyaan lebih lanjut, jangan ragu untuk bertanya!

 --- END TUGAS 7 ---