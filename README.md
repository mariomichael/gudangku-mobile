TUGAS 1

1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter? <br />
Perbedaan utama antara keduanya adalah stateless widget merupakan widget yang tidak mempunyai state. Widget ini tidak berubah melalui serangkaian aksi yang dilakukan user. Mereka hanya diubah oleh external event dari parent widgetnya di dalam gadget tree. Sedangkan stateful widget adalah widget yang memiliki state dan keadaannya bisa berubah tergantung aksi/input yang dilakukan oleh user. <br />
Secara sederhana, stateless widget adalah tipe widget yang tidak memiliki keadaan internal yang dapat berubah dan bersifat immutable (setelah dibuat, propertinya tak bisa diubah). Widget ini biasanya digunakan untuk bagian yang tidak perlu pembaruan secara berkala seperti teks, gambar, atau ikon. Sedangkan stateful widget adalah tipe widget yang keadaan internalnya dapat berubah-ubah. Widget ini digunakan pada bagian yang harus merespon perubahan interaksi dari user. Widget ini cocok untuk bagian seperti input user dan animasi berdasarkan input tersebut. <br />
<br />

2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing. <br />
1. MaterialApp: Untuk melakukan konfigurasi material seperti tema <br />
2. ColorScheme: Mengatur skema warna aplikasi <br />
3. AppBar: Menampilkan bar aplikasi <br />
4. SingleChildScrollView: Menampilkan widget yang bisa discroll <br />
5. Scaffold: Sebagai struktur dasar aplikasi flutter <br />
6. ScaffoldMessanger: Mengurus snackbar ketika dipanggil <br />
7. Text: Menampilkan teks <br />
8. Padding: Memberikan padding/jarak ke childnya <br />
9. Column: Menampilkan child dengan vertical array <br />
10. Material: Memberikan efek design visual pada elemen <br />
11.	Inkwell: Area yang responsif terhadap sentuhan <br />
12.	Container: Memberikan style seperti painting dan sizing terhadap individu elemen <br />
13.	Center: Membuat child element di tengah <br />
14.	Icon: Menampilkan ikon design <br />
15.	SnackBar: Menampilkan pesan pada bagian bawah sesuai input <br />

3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial) <br />
-	Membuat sebuah program Flutter baru dengan tema inventory seperti tugas-tugas sebelumnya. <br />
Pertama, saya membuat repository baru di GitHub dengan nama “gudangku-mobile”. Setelah itu saya membuat folder baru di Document untuk menyimpan proyek tugas saya.  Saya melakukan git init untuk menginisialisasi git, lalu menghubungkannya dengan repository di GitHub. <br />
Kedua, saya menjalankan “flutter create gudangku” pada direktori tersebut lalu masuk ke direktori proyek yang baru saya buat. Setelah itu saya coba menjalannkannya. <br />
Ketiga, saya mulai merapikan struktur proyek yang ada ketika menjalankan “flutter create”. Saya membuat file “menu.dart” pada direktori lib. Di sana saya mengimpor material.dart dan menambahkan class MyHomePage beserta statenya yang berasal dari file “main.dart”. Pada “main.dart” saya mengimpor file “menu.dart” yang baru saja saya buat. <br />
<br />
-	Membuat tiga tombol sederhana dengan ikon dan teks untuk melihat daftar item (Lihat Item), menambah item (Tambah Item), dan logout (Logout) <br />
Pertama, saya mengubah sifat widget halaman menu menjadi stateless dengan cara mengubah constructornya dan menambahkan widget build dengan kode seperti yang terterta di tutorial. Saya juga menghapus function statenya karena sekarang widgetnya stateless. <br />
Kedua, saya membuat class ShopItem yang memiliki field name, icon, dan color (bonus). Lalu saya membuat list dari items yang berisi “Lihat Item”, “Tambah Item”, dan “Logout”. Setelah itu saya melengkapi kode di dalam widget build dengan kode yang ada di tutorial. Lalu saya menambahkan class ShopCard yang stateless untuk menampilkan card. <br />
<br />
-	Memunculkan Snackbar dengan tulisan tertentu ketika tombol ditekan<br />
Saya melakukan ini dengan menambahkan “ScaffoldMessanger” dengan konten tulisan yang akan keluar ketika tombol ditekan pada widget build di class ShopCard pada file “menu.dart”. <br />
Terakhir, saya melakukan git add, commit, dan push setelah aplikasi pada tugas kali ini selesai. <br />
