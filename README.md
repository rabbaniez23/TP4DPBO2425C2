# TP4DPBO2425C2
gui java


# Laporan Proyek - Aplikasi CRUD Manajemen Produk

Aplikasi ini adalah program desktop sederhana yang dibuat menggunakan Java Swing untuk mengelola data produk. Program ini memungkinkan pengguna untuk melakukan operasi CRUD (Create, Read, Update, Delete) pada daftar produk.

## Struktur Folder
```
.
├── ProductData/                # Folder utama proyek (source code)
│   ├── Product.java
│   └── ProductMenu.java
├── Dokumentasi/                # Folder berisi screenshot untuk README
│   
│   
│   
│   
└── README.md                   # File ini
```

## Desain Program
Aplikasi ini dirancang dengan satu window utama (`JFrame`) yang berisi semua komponen yang diperlukan untuk manajemen data.

* **Teknologi**: Java Swing
* **Struktur Data**: Data produk disimpan sementara di dalam `ArrayList<Product>` selama program berjalan.
* **Komponen Utama**:
    * `JTable`: Untuk menampilkan daftar produk dalam bentuk tabel.
    * `JTextField`: Untuk input ID, Nama, dan Harga produk.
    * `JComboBox`: Untuk memilih Kategori produk.
    * `JSlider`: Untuk menentukan Stok produk.
    * `JButton`: Terdapat 3 tombol utama:
        1.  **Add/Update**: Tombol dinamis yang berfungsi untuk menambah data baru atau menyimpan perubahan data yang sudah ada.
        2.  **Delete**: Untuk menghapus data yang dipilih dari tabel.
        3.  **Cancel**: Untuk membatalkan aksi dan membersihkan form input.

## Penjelasan Alur Program

Berikut adalah alur penggunaan aplikasi untuk setiap operasi CRUD:

1.  **Menampilkan Data (Read)**
    * Saat aplikasi pertama kali dijalankan, program akan secara otomatis memuat data produk awal dari method `populateList()` dan menampilkannya di dalam `JTable`.

2.  **Menambahkan Data (Create)**
    * Pengguna mengisi semua field pada form (ID Produk, Nama, Harga, Kategori, dan Stok).
    * Saat form diisi, tombol utama akan berlabel "Add".
    * Setelah menekan tombol **"Add"**, data baru akan ditambahkan ke `ArrayList` dan tabel akan diperbarui secara otomatis.
    * Form input akan dikosongkan kembali.

3.  **Mengubah Data (Update)**
    * Pengguna mengklik salah satu baris data pada `JTable`.
    * Data dari baris yang dipilih akan otomatis muncul di form input.
    * Tombol "Add" akan berubah teks menjadi **"Update"**, dan tombol "Delete" akan muncul.
    * Pengguna mengubah data yang diinginkan pada form.
    * Setelah menekan tombol **"Update"**, data pada `ArrayList` akan diperbarui sesuai indeks yang dipilih, dan tampilan tabel akan diperbarui.
    * Form input akan dikosongkan kembali.

4.  **Menghapus Data (Delete)**
    * Pengguna mengklik salah satu baris data pada `JTable`.
    * Tombol **"Delete"** akan muncul.
    * Saat tombol **"Delete"** ditekan, sebuah dialog konfirmasi akan tampil untuk memastikan pengguna yakin ingin menghapus data.
    * Jika pengguna memilih "Yes", data akan dihapus dari `ArrayList` dan tabel akan diperbarui.
    * Form input akan dikosongkan kembali.

5.  **Membatalkan Aksi (Cancel)**
    * Tombol **"Cancel"** berfungsi untuk membersihkan semua field input pada form dan mengembalikan state tombol ke mode "Add" (menyembunyikan tombol "Delete" dan mengubah teks tombol "Update" menjadi "Add").

## Dokumentasi Saat Program Dijalankan

Berikut adalah dokumentasi penggunaan program yang menunjukkan semua operasi CRUD.

### 1. Tampilan Awal (Read)
Tampilan saat program pertama kali dibuka. Semua data awal berhasil dimuat dan ditampilkan pada tabel.

<img width="930" height="692" alt="Screenshot 2025-10-06 080638" src="https://github.com/user-attachments/assets/6d54fdba-aead-44ca-a429-4e8b41dfeaf2" />


### 2. Proses Menambahkan Data (Create)
Demonstrasi proses pengisian form dan penambahan data baru ke dalam tabel.

<img width="879" height="756" alt="Screenshot 2025-10-06 080646" src="https://github.com/user-attachments/assets/242642f5-d59a-4eb2-bdc3-78e942c838d3" />


<img width="879" height="756" alt="Screenshot 2025-10-06 080646" src="https://github.com/user-attachments/assets/f7d3dd2f-5e85-4b05-9e20-b7d37f6dceef" />


### 3. Proses Mengubah Data (Update)
Demonstrasi proses memilih data dari tabel, mengubah isinya melalui form, dan menyimpannya.

<img width="875" height="706" alt="Screenshot 2025-10-06 080714" src="https://github.com/user-attachments/assets/8d5bd957-d0d9-4a00-b159-64e803d463c2" />

<img width="871" height="729" alt="Screenshot 2025-10-06 080721" src="https://github.com/user-attachments/assets/eb81babe-72bd-4063-95b3-76f24b88142c" />


### 4. Proses Menghapus Data (Delete)
Demonstrasi proses memilih data dari tabel, menekan tombol hapus, dan melakukan konfirmasi penghapusan.

<img width="835" height="755" alt="Screenshot 2025-10-06 080736" src="https://github.com/user-attachments/assets/597f1d1b-c31b-4221-8907-ad4bf7da3f5b" />

<img width="821" height="730" alt="Screenshot 2025-10-06 080746" src="https://github.com/user-attachments/assets/57e03457-f0f1-4bfe-8dfa-7b2ab173309c" />


