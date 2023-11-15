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


 --- START TUGAS 8 ---

 1. Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat!
`Navigator.push()`
Fungsi Navigator.push() digunakan untuk menambahkan rute baru ke dalam tumpukan navigator, memungkinkan pengguna kembali ke rute sebelumnya melalui tombol kembali atau gestur kembali. Sebagai contoh, dalam aplikasi dengan daftar produk, metode ini bisa digunakan untuk beralih ke halaman detail produk saat pengguna ingin melihat informasi lebih lanjut.

`Navigator.pushReplacement()`
Metode Navigator.pushReplacement() digunakan untuk menggantikan rute saat ini dengan rute baru dalam tumpukan navigator. Hal ini bermanfaat ketika Anda tidak ingin pengguna kembali ke rute sebelumnya. Contoh penggunaan umum adalah dalam skenario login atau logout, di mana setelah pengguna berhasil login, Anda tidak ingin mereka dapat kembali ke halaman login dengan menekan tombol kembali.

 2. Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing!
 `Container`: Diperlukan untuk menghias child widget dengan menentukan warna, batas, margin, dan ruang padding. Juga dapat digunakan untuk melakukan transformasi geometrik pada widget.

`Column & Row`: Berfungsi untuk mengatur tata letak secara vertikal (Column) atau horizontal (Row). Baik Column maupun Row dapat memiliki beberapa child widgets.

`Stack`: Mengizinkan widget untuk ditumpuk satu di atas yang lain, berguna untuk menempatkan widget di atas widget lain, seperti membuat latar belakang dengan teks di atasnya.

`Wrap`: Mirip dengan Row atau Column, tetapi dapat beralih secara otomatis ke baris atau kolom berikutnya jika tidak ada cukup ruang.

`Padding`: Menambahkan ruang tambahan di sekitar child widget-nya.

`Align & Center`: Digunakan untuk menentukan posisi widget dalam parent widget. Center digunakan untuk memusatkan child di dalamnya.

`Expanded & Flexible`: Memberikan child widget fleksibilitas dalam hal ukuran, dapat mengisi ruang yang tersedia atau menyesuaikan ukurannya sesuai dengan faktor flex.

`ListView`: Digunakan untuk membuat daftar yang dapat di-scroll dan menampung banyak children.

`GridView`: Layout berbentuk grid yang dapat di-scroll, berguna untuk menampilkan banyak data dalam bentuk grid.

`ConstrainedBox & SizedBox`: Digunakan untuk membatasi ukuran widget child, baik secara spesifik atau dengan batasan tertentu.

`AspectRatio`: Memaksa child widget untuk memiliki rasio aspek tertentu.

`FractionallySizedBox`: Menetapkan ukuran widget child sebagai persentase tertentu dari ukuran parent widget.

`Table`: Menyusun widgets dalam format tabel dengan baris dan kolom yang tetap.

`Flow`: Memberikan kontrol penataan yang lebih kompleks, memungkinkan pembuatan layout yang tidak dapat dicapai dengan menggunakan Row atau Column.

`RichText`: Memungkinkan penggabungan teks dengan gaya yang berbeda di dalam satu paragraf.

 3. Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut!
 `TextFormField` untuk Nama Item: 
**Alasan Penggunaan:** Input ini dimanfaatkan untuk mengumpulkan nama item yang akan ditambahkan. Ini merupakan informasi pokok yang diperlukan untuk setiap barang yang ada di dalam toko.

`TextFormField` untuk Jumlah (Amount): 
**Alasan Penggunaan:** Input ini dirancang khusus untuk menggali jumlah atau kuantitas dari suatu item. Menggunakan input teks yang dikonversi menjadi integer memungkinkan validasi input guna memastikan bahwa pengguna memasukkan nilai numerik dengan benar.

`TextFormField` untuk Deskripsi: 
**Alasan Penggunaan:** Input ini dimanfaatkan untuk mendapatkan deskripsi tambahan tentang item. Deskripsi ini dapat berisi informasi rinci yang mungkin tidak tercakup hanya dengan menyebutkan nama item, seperti ukuran, warna, atau fitur-fitur spesifik lainnya.

 4. Bagaimana penerapan clean architecture pada aplikasi Flutter?
 Penggunaan clean architecture dalam pengembangan aplikasi Flutter bertujuan untuk memisahkan kode ke dalam berbagai lapisan yang saling bekerja secara independen. Tujuannya adalah untuk mempermudah proses pengujian, pemeliharaan, dan meningkatkan skalabilitas aplikasi. Berikut adalah lapisan-lapisan umum dalam clean architecture yang dapat diimplementasikan dalam konteks Flutter:

Layer Presentasi: Tempat penyimpanan semua kode yang terkait dengan antarmuka pengguna (UI).

Layer Domain: Merupakan lapisan inti yang menetapkan logika bisnis dari aplikasi.

Layer Data: Bertanggung jawab untuk mengimplementasikan antarmuka Repository yang telah ditetapkan di dalam layer domain.

Layer Infrastruktur (opsional): Berfungsi sebagai ekstensi dari layer data.

 5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial)
 Untuk membuat satu halaman baru pada aplikasi, yaitu halaman formulir tambah item baru dengan ketentuan sebagai berikut:

1. Buatlah file `shoplist_form.dart` pada direktori `lib`.
```dart
import 'package:flutter/material.dart';
import 'package:mart_project/widgets/left_drawer.dart';

class ShopFormPage extends StatefulWidget {
  const ShopFormPage({Key? key}) : super(key: key);

  @override
  State<ShopFormPage> createState() => _ShopFormPageState();
}

class _ShopFormPageState extends State<ShopFormPage> {
  @override
  Widget build(BuildContext context) {
    return Placeholder();
  }
}
```

2. Tambahkan minimal tiga elemen input: `name`, `amount`, dan `description`. Sesuaikan elemen input dengan model pada aplikasi tugas Django yang telah dibuat.
```dart
class _ShopFormPageState extends State<ShopFormPage> {
  final _formKey = GlobalKey<FormState>();
  String _name = "";
  int _price = 0;
  int _size = 0;
  int _amount = 0;
  String _description = "";
  
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Center(
          child: Text('Form Tambah Item'),
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
              // ... (input elements)
            ],
          ),
        ),
      ),
      bottomNavigationBar: Align(
        alignment: Alignment.bottomCenter,
        child: Padding(
          padding: const EdgeInsets.all(8.0),
          child: ElevatedButton(
            style: ButtonStyle(
              backgroundColor: MaterialStateProperty.all(Colors.green[900]),
            ),
            onPressed: () {
              // ... (save button logic)
            },
            child: const Text(
              "Save",
              style: TextStyle(color: Colors.white),
            ),
          ),
        ),
      ),
    );
  }
}
```

3. Validasi setiap elemen input sesuai ketentuan yang telah ditentukan.
```dart
validator: (String? value) {
  if (value == null || value.isEmpty) {
    return "Nama tidak boleh kosong!";
  }
  return null;
},
```

4. Arahkan pengguna ke halaman form tambah item baru ketika menekan tombol Tambah Item pada halaman utama.
```dart
// pada file shop_card.dart
if (item.name == "Tambah Item") {
  Navigator.push(
    context,
    MaterialPageRoute(builder: (context) => ShopFormPage()),
  );
}
```

5. Tampilkan data yang diisi dalam formulir pada sebuah pop-up setelah menekan tombol Save.
```dart
// pada file shoplist_form.dart
onPressed: () {
  if (_formKey.currentState!.validate()) {
    showDialog(
      context: context,
      builder: (context) {
        return AlertDialog(
          title: const Text('Item berhasil tersimpan!'),
          content: SingleChildScrollView(
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: [
                Text('Nama: $_name'),
                Text('Harga: $_price'),
                Text('Ukuran: $_size'),
                Text('Jumlah: $_amount'),
                Text('Deskripsi: $_description'),
                // TODO: Munculkan value-value lainnya
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
```

6. Tambahkan drawer pada aplikasi dengan minimal dua opsi: Halaman Utama dan Tambah Item.
```dart
// pada file left_drawer.dart
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
  title: const Text('Tambah Item'),
  onTap: () {
    Navigator.pushReplacement(
      context,
      MaterialPageRoute(builder: (context) => ShopFormPage()),
    );
  },
),
```

 --- END TUGAS 8 ---