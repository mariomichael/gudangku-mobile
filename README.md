TUGAS 2

# Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat!
Perbedaan keduanya adalah Navigator.push() digunakan untuk menambahkan suatu route ke dalam stack route yang dikelola oleh Navigator. Ketika method ini digunakan, halaman baru ditambahkan ke atas stack. Pengguna dapat kembali ke halaman sebelumnya dengan menekan tombol “back” di perangkat tersebut. Method ini akan menambahkan halaman baru ke dalam tumpukan navigasi. Method ini cocok digunakan ketika ingin kembali ke halaman-halaman sebelumnya yang sudah dikunjungi. Misalnya ketika sedang mengisi form yang terdiri dari beberapa page, ada tombol “back” agar pengguna bisa kembali ke halaman sebelumnya dan mengganti data yang ternyata salah input.
Sedangkan Navigator.pushReplacement() digunakan untuk menghapus route yang sedang ditampilkan kepada pengguna dan menggantinya dengan route lain. Ketika method ini digunakan dan berjalan, aplikasi akan berpindah dari route yang sedang ditampilkan kepada pengguna ke suatu route yang diberikan. Route lama pada stack route yang dikelola Navigator akan digantikan secara langsung oleh route baru tanpa mengubah kondisi elemen stack di bawahnya. Method ini cocok digunakan ketika tidak ingin pengguna kembali ke layar yang sebelumnya ditampilkan, misalnya ketika ingin melakukan login, dengan adanya method tersebut, pengguna tidak bisa kembali back ke halaman login setelah berhasil login ke aplikasi tersebut. <br />

# Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing!
Align: Widget yang menyamakan posisi childnya dengan dirinya dan secara opsional menyesuaikan ukurannya berdasarkan ukuran child tersebut.
AspectRatio: Widget yang mencoba menyesuaikan ukuran childnya ke aspek rasio yang spesifik
Center: Blok penyesuaian yang menegahkan childnya dalam dirinya sendiri
Container: Widget yang digunakan sebagai pembungkus yang menyatukan widget painting, positioning, dan sizing
Padding: Widget yang memberikan padding pada childnya sesuai dengan padding yang diberikan
Column: Widget yang berfungsi untuk menata daftar child widget secara vertikal
Row: Widget yang berfungsi untuk menata daftar child widget secara horizontal
ListView: Merupakan daftar widget linear ke bawah yang bisa discroll <br />

# Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut!
Saya hanya menggunakan element input TextField. Saya menggunakan elemen ini untuk menginput nama, jumlah, dan deskripsi produk. Elemen ini digunakan karena ketiga input yang saya berikan hanya menerima input teks. <br />

# Bagaimana penerapan clean architecture pada aplikasi Flutter?
Penerapan clean architecture pada aplikasi Flutter adalah dengan membagi aplikasi menjadi beberapa layer, yaitu domain layer (untuk mendefinisikan objek domain atau model bisnis), data layer (untuk berinteraksi dengan database dan mengurus data), dan presentation layer (untuk menampilkan informasi kepada pengguna dan menerima input dari pengguna), serta outer layer (layer paling luar yang berisi detail implementasi teknis). Ketika menulis code, pisahkan setiap bagian ke dalam layer-layer tersebut sesuai fungsinya agar lebih mudah didebug ketika ada suatu error. Bisa juga menggunakan konsep abstract dan implement agar kode di dalam layer tertentu tidak tergantung pada implementasi spesifik di bagian lain. Selain itu dapat digunakan State Management, yaitu degan menggunakan konsep BLoC (Business Logic Components) sehingga dapat menguji logika bisnis secara terpisah dari tampilan UI. Dependency pada proyek juga harus diperhatikan. <br />

# Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial)
-	Membuat minimal satu halaman baru pada aplikasi, yaitu halaman formulir tambah item baru dengan ketentuan emakai minimal tiga elemen input, yaitu name, amount, description. Tambahkan elemen input sesuai dengan model pada aplikasi tugas Django yang telah kamu buat, memiliki sebuah tombol Save, dan setiap elemen input di formulir juga harus divalidasi.

Saya melakukan checklist ini dengan pertama-tama membuat berkas baru di direktori lib yang akan mengurus form tersebut. Saya mengisinya dengan impor material yang dibutuhkan dan widget Scaffold yang berisi form yang akan menerima input. Saya membuat beberapa variable untuk menyimpan input dari tiap field. Selanjutnya saya membuat widget column agar tampilan memanjang ke bawah. Saya lalu membuat widget TextFormField untuk menerima input teks yang saya beri tambahan padding dan beberapa atribut lain. Saya lalu membuat tombol “Save” untuk menyimpan input tersebut. Saya juga menggunakan fungsi showDialog() dan AlertDialog() untuk mengurus masalah input yang tidak sesuai.

-	Mengarahkan pengguna ke halaman form tambah item baru ketika menekan tombol Tambah Item pada halaman utama.

Saya mengimplementasikan checklist ini dengan menambah navigasi jika tombol “Tambah Item” diklik, maka akan diarahkan ke ShopForm.

-	Memunculkan data sesuai isi dari formulir yang diisi dalam sebuah pop-up setelah menekan tombol Save pada halaman formulir tambah item baru.

Saya mengimplementasikan checklist ini dengan menambahkan function showDialog() dan AlertDialog() dan function reset form untuk mengatur input baik yang formatnya tidak sesuai maupun yang telah sesuai format.

-	Membuat sebuah drawer pada aplikasi dengan ketentuan drawer minimal memiliki dua buah opsi, yaitu Halaman Utama dan Tambah Item, ketika memiih opsi Halaman Utama, maka aplikasi akan mengarahkan pengguna ke halaman utama, ketika memiih opsi (Tambah Item), maka aplikasi akan mengarahkan pengguna ke halaman form tambah item baru.

Saya mengimplementasi checklist ini dengan membuat folder baru bernama widgets lalu membuat file “left_drawer.dart” dan mengisinya dengan widget build yang memiliki child ListView, saya menambahkan impor yang dibutuhkan, selanjutnya saya menambahkan naviasi ke halaman Form dan Main di bagian routing. Selanjutnya saya menambahkan dekorasi pada drawer saya dengan menambahkan kode di bagian head. Saya menggunakan Navigator.push() juga agar pengguna dapat melakukan back.

Itulah cara saya mengimplementasikan semua checklist yang ada. <br />



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