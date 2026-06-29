## Lab11Web_VueJs Lanjutan 11-14

# Praktikum 11 - VueJS

# Tujuan Praktikum

- Memahami konsep dasar API.
- Memahami konsep dasar Framework VueJS.
- Membuat Frontend API menggunakan VueJS 3.

---

# Langkah-langkah Praktikum

## 1. Membuat Project VueJS

Membuat project baru dengan struktur folder sebagai berikut.

```text
lab8_vuejs/
│
├── index.html
│
└── assets
    ├── css
    │   └── style.css
    └── js
        └── app.js
```

---

## 2. Menambahkan Library VueJS dan Axios

Menambahkan library VueJS dan Axios menggunakan CDN pada file `index.html`.

```html
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
```

Library VueJS digunakan untuk membangun tampilan aplikasi, sedangkan Axios digunakan untuk mengakses REST API.

---

## 3. Menampilkan Data Artikel

Data artikel diambil dari REST API menggunakan Axios.

```javascript
axios.get(apiUrl + '/post')
```

Data ditampilkan menggunakan directive `v-for`.

Fitur yang ditampilkan meliputi:

- ID Artikel
- Judul Artikel
- Status
- Tombol Edit
- Tombol Hapus

---

## 4. Membuat Form Tambah Data

Menambahkan tombol **Tambah Data** yang akan membuka form dalam bentuk modal.

Field yang tersedia yaitu:

- Judul
- Isi Artikel
- Status

Data dikirim menggunakan method **POST**.

<img width="1366" height="720" alt="vue1 11" src="https://github.com/user-attachments/assets/044ae8b7-1282-4e0e-b009-edb94ca80ef9" />

<img width="1366" height="720" alt="vue2" src="https://github.com/user-attachments/assets/b5705939-8211-492b-b590-a2077e1b96f6" />

---

## 5. Membuat Fitur Edit Data

Saat tombol **Edit** dipilih, data artikel akan ditampilkan pada form untuk diubah.

Perubahan data dikirim menggunakan method **PUT**.

<img width="1366" height="720" alt="vue3" src="https://github.com/user-attachments/assets/83cb40df-cf2e-4cdd-8c52-2a8e04180f8b" />

<img width="1366" height="720" alt="vue4" src="https://github.com/user-attachments/assets/3690ffe1-0fa1-47f8-8b00-6d3b6247eee6" />

---

## 6. Membuat Fitur Hapus Data

Saat tombol **Hapus** dipilih, sistem akan menampilkan konfirmasi terlebih dahulu.

Jika pengguna memilih **OK**, maka data akan dihapus menggunakan method **DELETE**.

<img width="1366" height="720" alt="vue hapus 5" src="https://github.com/user-attachments/assets/7d8faf2a-b67a-40fd-9758-42226638bf8f" />

<img width="1366" height="720" alt="vue6" src="https://github.com/user-attachments/assets/b77855bb-be5d-4caa-a6e1-8a539632c402" />

---

## 7. Membuat Tampilan CSS

File `style.css` digunakan untuk mempercantik tampilan aplikasi.

Style diterapkan pada:

- Tabel
- Tombol
- Form
- Modal
- Header
- Layout halaman

Sehingga tampilan aplikasi menjadi lebih menarik dan mudah digunakan.

---

# Hasil Praktikum

Hasil akhir aplikasi berhasil menjalankan operasi CRUD menggunakan VueJS dan REST API CodeIgniter 4 tanpa melakukan reload halaman.

---

# Kesimpulan

Pada praktikum ini berhasil dibuat aplikasi frontend menggunakan VueJS 3 yang terhubung dengan REST API CodeIgniter 4. VueJS mempermudah pengelolaan tampilan melalui konsep reactive data binding, sedangkan Axios digunakan untuk melakukan komunikasi dengan REST API tanpa melakukan reload halaman. Dengan demikian aplikasi menjadi lebih interaktif, responsif, dan mudah dikembangkan.

---

# Praktikum 12 - VueJS Komponen dan Routing (Single Page Application)

Pada praktikum ini dilakukan pengembangan aplikasi VueJS dengan menerapkan konsep **Vue Component** dan **Vue Router** sehingga aplikasi dapat berjalan sebagai **Single Page Application (SPA)**. Dengan Vue Router, perpindahan halaman dapat dilakukan tanpa melakukan reload browser.

---

## 1. Menambahkan Library Vue Router

Menambahkan library **Vue Router** melalui CDN pada file `index.html`.

---

## 2. Membuat Komponen Home

Membuat file `Home.js` pada folder `assets/js/components` sebagai halaman beranda yang menampilkan informasi selamat datang kepada pengguna.

---

## 3. Membuat Komponen Artikel

Memindahkan seluruh fitur CRUD artikel ke dalam file `Artikel.js` sehingga kode menjadi lebih terstruktur dan mudah dikelola.

Fitur yang tersedia:
- Menampilkan data artikel.
- Menambah artikel.
- Mengubah artikel.
- Menghapus artikel.

---

## 4. Mengatur Vue Router

Melakukan konfigurasi routing pada file `app.js` dengan menambahkan route untuk halaman **Beranda** dan **Kelola Artikel** menggunakan `createRouter()` dan `createWebHashHistory()`.

---

## 5. Memodifikasi Halaman Utama

Memodifikasi file `index.html` dengan menambahkan:

- `router-link` sebagai menu navigasi.
- `router-view` sebagai tempat menampilkan halaman sesuai route.

---

## 6. Menambahkan CSS

Menambahkan style untuk menu navigasi, halaman Home, dan route aktif agar tampilan aplikasi menjadi lebih menarik.

---

## 7. Menambahkan Halaman About

Membuat file `About.js` yang berisi:

- Nama
- NIM
- Kelas
- Foto/Avatar

Selanjutnya menambahkan route `/about` pada `app.js` serta menu **About** pada navigasi aplikasi.

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/a4b0ecfa-79c5-4c05-81a6-60b837d4caea" />

# 8. Tampilan beranda

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/cb70dff2-5dbb-47c5-b4bd-a9a97d174534" />

# 9. Tampilan kelola artikel

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/be081619-1a91-45a5-8aff-deea5a8bd1ee" />

---

# Hasil Praktikum

Setelah seluruh langkah selesai, aplikasi berhasil berjalan sebagai **Single Page Application (SPA)** menggunakan VueJS dan Vue Router.

---

# Praktikum 13 - VueJS Autentikasi dan Navigation Guards (SPA Security)

## Deskripsi
Praktikum ini membahas implementasi sistem autentikasi pada aplikasi Single Page Application (SPA) menggunakan VueJS 3 dan Vue Router. Selain itu, dibuat juga REST API Login pada backend CodeIgniter 4 yang digunakan untuk memvalidasi data pengguna. Proteksi halaman dilakukan menggunakan Navigation Guards (`beforeEach`) sehingga hanya pengguna yang telah login yang dapat mengakses halaman admin.

---

## Tujuan Praktikum

- Memahami konsep keamanan pada aplikasi Single Page Application (SPA).
- Memahami penggunaan Navigation Guards pada Vue Router.
- Membuat API Login menggunakan CodeIgniter 4.
- Menghubungkan frontend VueJS dengan backend melalui REST API.
- Mengimplementasikan sistem Login, Logout, dan proteksi halaman menggunakan Local Storage.

---

## Langkah-langkah Praktikum

### 1. Membuat API Login pada Backend CodeIgniter 4

Membuat controller `Auth.php` pada folder:

```text
app/Controllers/Api/Auth.php
```

Controller ini berfungsi untuk:

- menerima username dan password dari frontend
- melakukan validasi data pengguna
- mengirimkan response JSON
- menghasilkan token sederhana apabila login berhasil

---

### 2. Menambahkan Route Login

Menambahkan route pada file:

```php
app/Config/Routes.php
```

```php
$routes->post('api/login', 'Api\Auth::login');
```

Route tersebut digunakan sebagai endpoint proses autentikasi.

---

### 3. Membuat Komponen Login VueJS

Membuat file:

```text
assets/js/components/Login.js
```

Komponen Login memiliki fitur:

- Form Username / Email
- Form Password
- Validasi Login menggunakan Axios
- Menyimpan status login ke Local Storage
- Redirect ke halaman Artikel setelah login berhasil

---

### 4. Konfigurasi Vue Router

Melakukan konfigurasi pada:

```text
assets/js/app.js
```

Penambahan meliputi:

- Route Home
- Route Login
- Route Artikel
- Meta `requiresAuth`
- Navigation Guards (`beforeEach`)

Navigation Guard digunakan untuk mengecek apakah pengguna sudah login sebelum mengakses halaman Artikel.

---

### 5. Menambahkan Menu Login dan Logout

File yang dimodifikasi:

```text
index.html
```

Menu navigasi dibuat dinamis menggunakan Vue.

Sebelum login:

- Beranda
- Kelola Artikel
- Login

Sesudah login:

- Beranda
- Kelola Artikel
- Logout

---

### 6. Menambahkan Tampilan Login

Menambahkan CSS pada:

```text
assets/css/style.css
```

Agar tampilan Login memiliki:

- posisi di tengah halaman
- tampilan modern
- tombol login
- pesan error ketika login gagal

---

## Pengujian

### Skenario A

Pengguna belum login.

Hasil:

- ketika membuka menu **Kelola Artikel**
- sistem menampilkan alert
- pengguna otomatis diarahkan ke halaman Login

✅ Berhasil

---

### Skenario B

Pengguna login menggunakan akun yang valid.

Hasil:

- Login berhasil
- Token tersimpan di Local Storage
- Halaman Artikel dapat diakses
- Menu Login berubah menjadi Logout

✅ Berhasil

---

## Hasil Praktikum

Praktikum ini berhasil mengimplementasikan sistem autentikasi pada aplikasi SPA menggunakan VueJS dan CodeIgniter 4.

Fitur yang berhasil dibuat:

- REST API Login
- Form Login menggunakan VueJS
- Axios untuk komunikasi API
- Penyimpanan status login menggunakan Local Storage
- Navigation Guards Vue Router
- Proteksi halaman admin
- Logout

---

## Dokumentasi

### Halaman Beranda

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/6717afd3-9ea1-4fed-b1e7-285395c65eb8" />

---

### Halaman Login

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/795bdf60-baf8-449b-9b02-d0856f38cec3" />

---

### Login Berhasil

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/ad886d8e-97c9-4eda-a928-2b1aae4d7cf6" />

---

### Halaman Kelola Artikel

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/1360861f-d4fe-4bc4-8e77-b63e146db3d1" />

---

### Logout

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/fbe8880b-a4a9-4146-b115-f94846eeeaca" />

---

## Kesimpulan

Pada praktikum ini berhasil dibuat sistem autentikasi sederhana menggunakan REST API CodeIgniter 4 dan VueJS. Navigation Guards pada Vue Router mampu membatasi akses ke halaman tertentu sehingga hanya pengguna yang telah melakukan login yang dapat mengakses halaman administrasi. Dengan memanfaatkan Axios dan Local Storage, proses autentikasi dapat berjalan secara dinamis tanpa melakukan reload halaman, sehingga aplikasi bekerja sebagai Single Page Application (SPA).

---

# Praktikum 14 - Keamanan API, Autentikasi Token, dan Axios Interceptors

## Deskripsi

Pada praktikum ini dilakukan implementasi keamanan pada REST API menggunakan **Token-Based Authentication** pada backend CodeIgniter 4 serta **Axios Interceptors** pada frontend VueJS. Selain itu diterapkan **API Filters** untuk melindungi endpoint dari akses ilegal sehingga hanya pengguna yang memiliki token yang dapat melakukan proses tambah, ubah, dan hapus data artikel.

---

## Tujuan Praktikum

- Memahami konsep Token-Based Authentication pada REST API.
- Mengimplementasikan API Filter pada CodeIgniter 4.
- Memahami penggunaan Axios Interceptors pada VueJS.
- Mengamankan komunikasi antara frontend dan backend menggunakan Authorization Token.

---

## Langkah-langkah Praktikum

### 1. Membuat API Authentication Filter

Membuat file baru:

```text
app/Filters/ApiAuthFilter.php
```

Filter digunakan untuk memeriksa Authorization Header dan memastikan request membawa Bearer Token yang valid.

---

### 2. Mendaftarkan Filter

Menambahkan filter pada file:

```text
app/Config/Filters.php
```

Kemudian menambahkan alias:

```php
'apiauth' => \App\Filters\ApiAuthFilter::class,
```

---

### 3. Mengamankan Endpoint REST API

Mengubah file:

```text
app/Config/Routes.php
```

Filter diterapkan pada endpoint:

- POST `/post`
- PUT `/post/{id}`
- DELETE `/post/{id}`

Sehingga hanya request yang memiliki token yang dapat mengakses endpoint tersebut.

---

### 4. Menambahkan Axios Interceptors

Melakukan konfigurasi pada file:

```text
assets/js/app.js
```

Axios Interceptors digunakan untuk:

- Mengambil token dari Local Storage.
- Menambahkan Authorization Header secara otomatis.
- Menangani response **401 Unauthorized**.
- Mengarahkan pengguna kembali ke halaman Login apabila token tidak valid.

---

### 5. Pengujian Menggunakan Postman

Melakukan request POST ke endpoint `/post` tanpa Authorization Header.

Hasil pengujian:

- Server menolak request.
- Response menampilkan **HTTP 401 Unauthorized**.
- Endpoint API berhasil diamankan.

---

### 6. Pengujian Melalui Browser

Melakukan login melalui aplikasi VueJS kemudian mencoba fitur:

- Tambah Artikel
- Ubah Artikel
- Hapus Artikel

Semua proses berhasil karena Axios Interceptors secara otomatis mengirimkan Bearer Token pada setiap request.

---

## Hasil Praktikum

Praktikum ini berhasil mengimplementasikan keamanan REST API menggunakan Token-Based Authentication pada CodeIgniter 4 dan Axios Interceptors pada VueJS. Endpoint yang dilindungi hanya dapat diakses oleh pengguna yang telah melakukan login dan memiliki token yang valid.

---

## Perbedaan Navigation Guards dan CodeIgniter Filters

| Navigation Guards | CodeIgniter Filters |
|-------------------|---------------------|
| Berjalan di sisi client. | Berjalan di sisi server. |
| Mengontrol perpindahan halaman SPA. | Mengamankan endpoint REST API. |
| Memeriksa status login dari Local Storage. | Memvalidasi Bearer Token pada request. |
| Tidak dapat mencegah akses API melalui Postman. | Dapat menolak request ilegal dengan status 401 Unauthorized. |

---

## Dokumentasi

### Error 401 Unauthorized

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/aeee66a8-7b33-4dd0-8a25-6c04b458fb8d" />

---

### Axios Interceptors

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/1797e543-e597-4d62-a06a-181afff377fc" />

<img width="1366" height="720" alt="image" src="https://github.com/user-attachments/assets/29274cf4-2704-4f13-ad0c-a4fd0636adab" />

---

## Kesimpulan

Pada praktikum ini berhasil diterapkan sistem keamanan REST API menggunakan Token-Based Authentication melalui CodeIgniter Filters dan Axios Interceptors. Penggunaan Navigation Guards hanya berfungsi membatasi akses pada sisi client, sedangkan CodeIgniter Filters memberikan perlindungan pada sisi server sehingga endpoint API tidak dapat diakses tanpa token yang valid.

---
