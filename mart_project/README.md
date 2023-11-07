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

 --- END TUGAS 7 ---