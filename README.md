# TUTORIAL 2

## 2.1. Original code of broadcast chat.

![alt text](image.png)

Untuk menjalankan program tersebut, langkah pertama adalah membuka empat terminal atau command prompt. Di terminal pertama, jalankan server menggunakan perintah `cargo run --bin server`. Server akan mulai dan siap menerima koneksi dari client. Selanjutnya, buka tiga terminal tambahan untuk menjalankan tiga client dengan perintah `cargo run --bin client`.

Setelah semua client berhasil terhubung ke server, pengguna dapat mulai berinteraksi dengan program. Ketika pengguna mengetikkan pesan di salah satu client dan mengirimkannya, pesan tersebut akan dikirimkan ke server. Server kemudian akan meneruskan pesan tersebut ke semua client yang terhubung. Ini memungkinkan setiap client untuk menerima dan melihat pesan yang dikirim oleh client lainnya.

Contoh interaksi yang terjadi adalah sebagai berikut: jika pengguna mengetikkan pesan di Client 1 dan mengirimkannya, pesan tersebut akan terlihat di terminal server sebagai penerima pesan. Server akan mengirimkan pesan tersebut kembali ke Client 1, Client 2, dan Client 3. Akibatnya, setiap client akan menerima pesan yang dikirim oleh client lainnya, dan pesan tersebut juga akan muncul di terminal server sebagai perantara komunikasi.

Dengan demikian, program ini memfasilitasi komunikasi antara client yang terhubung melalui server sebagai perantara. Pesan-pesan yang dikirim dari satu client akan diterima oleh semua client lainnya, memungkinkan interaksi dan pertukaran informasi antara pengguna yang menggunakan aplikasi ini.

