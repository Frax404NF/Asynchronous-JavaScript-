## Basic Penerapan asynchronous JavaScript request menggunakan XHR & Fetch API

![image](https://github.com/user-attachments/assets/c05f406b-8cea-4aaf-b445-4395caeabe83)

- Dokumentasi Dummy Books API |
https://books-api.dicoding.dev/#/

## **Rangkuman Asynchronous JavaScript Request**
### **Apa Itu Asynchronous JavaScript Request**

  Asynchronous JavaScript request adalah sebuah teknik pemrograman halaman web yang dibangun dengan kompleks dan dinamis menggunakan teknologi yang dikenal dengan XMLHttpRequest. Asynchronous JavaScript request memungkinkan halaman web diperbarui tanpa terjadinya proses muat ulang halaman. Inilah yang biasanya diterapkan ketika kita membangun aplikasi web SPA (Single Page App).

  Konsep asynchronous JavaScript request adalah membuat sebuah HTTP request. HTTP request adalah proses yang terjadi ketika client mengirimkan request kepada server untuk menyediakan aset atau berkas yang dibutuhkan untuk diproses ke client. Hasil yang diterima oleh client dari server merupakan HTTP response.

### **Web API**

Web API adalah interface yang disediakan oleh penyedia data agar dapat dikonsumsi oleh berbagai macam platform bahkan perangkat. Web API bekerja menggunakan salah satu pola standar yang dinamakan REST (Representational State Transfer). Data yang diterima atau dikirimkan pada pola REST dapat berupa text, JSON atau XML.

Ada banyak tipe atau method dalam implementasinya. Namun, hanya empat method yang biasa digunakan.

- GET: request data atau meminta informasi dari Web API.
- POST: request untuk menambahkan data baru.
- PUT: request untuk mengubah data yang tersedia.
- DELETE: request untuk menghapus data yang tersedia.

### **CORS**

CORS adalah mekanisme berbasis HTTP header yang memungkinkan server untuk menunjukkan alamat aslinya (domain, skema, atau port), selain alamat server itu sendiri dari client atau browser mana yang diizinkan untuk mengakses sumber dayanya.

### **JSON**

JSON adalah singkatan dari JavaScript Object Notation. Ia adalah format yang sering digunakan dalam pertukaran data. Saat ini, JSON banyak digunakan karena berbasis teks dan relatif mudah dibaca. Struktur JSON terbentuk dari dua literal data, yakni objek dan array.

Selain itu, JSON mendukung beberapa tipe data berikut.

- String
- Number
- Boolean
- Null
- Object
- Array

### **Request dengan XMLHttpRequest**

XMLHttpRequest atau XHR adalah class atau blueprint yang bertugas membuat HTTP request menggunakan JavaScript. Ada beberapa callback atau event yang biasa digunakan.

- onload: dijalankan ketika request berhasil diproses.
- onerror: dijalankan ketika request gagal untuk diproses.
- onreadystatechange: dijalankan ketika properti readyState dari objek XHR berubah.

Ada juga beberapa function penting yang perlu diterapkan ketika menggunakan XHR.

- open(): untuk menentukan HTTP method dan URL yang dituju.
- send(): untuk mengirimkan request ke server. Method ini juga berguna untuk menyematkan data ke body request.
- setRequestHeader(): untuk menambahkan HTTP header pada request yang dikirimkan.

Tidak hanya file JSON yang dapat dikirim, tetapi dokumen yang ter-serialized, seperti Blob, BufferSource, FormData, URLSearchParam, ReadableStream, atau USVString object. Jika tidak ada value yang dikirimkan melalui body request, nilai null-lah yang digunakan.

### **Request dengan Fetch API**

Fetch adalah cara baru dalam membuat network request dengan lebih mudah tanpa membuat instance dari suatu class. Fetch memanfaatkan Promise untuk mengatasi asynchronous process sehingga mengurasi penerapan callback.

Selain itu, Fetch dapat dituliskan dengan gaya asynchronous menggunakan async/await. Dalam penerapannya, network request dilakukan pada saat fungsi fetch tereksekusi. URL yang dituju dituliskan sebagai parameter pada fungsi tersebut.

Secara default, Fetch menggunakan method request GET jika secara eksplisit tidak kita tetapkan. Jika request berhasil diproses, Fetch akan mengembalikan promise resolve atau fulfilled dan membawa response object di dalamnya, sedangkan jika request gagal diproses, Fetch akan mengembalikan promise rejected serta response object bersamanya.

Jika HTTP request yang akan dikirim perlu menambahkan informasi pada HTTP header, kita dapat melakukannya dalam sebuah object dan diberikan sebagai parameter kedua dari fungsi fetch. Properti-properti yang dapat ditambahkan sebagai berikut.

- method: menentukan method request yang dikirimkan.
- headers: menyematkan HTTP header yang dibutuhkan.
- body: membawa data ke body request.
