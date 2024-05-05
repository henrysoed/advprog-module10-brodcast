# TUTORIAL 2

## 2.1. Original code of broadcast chat.

![alt text](image.png)

Untuk menjalankan program tersebut, langkah pertama adalah membuka empat terminal atau command prompt. Di terminal pertama, jalankan server menggunakan perintah `cargo run --bin server`. Server akan mulai dan siap menerima koneksi dari client. Selanjutnya, buka tiga terminal tambahan untuk menjalankan tiga client dengan perintah `cargo run --bin client`.

Setelah semua client berhasil terhubung ke server, pengguna dapat mulai berinteraksi dengan program. Ketika pengguna mengetikkan pesan di salah satu client dan mengirimkannya, pesan tersebut akan dikirimkan ke server. Server kemudian akan meneruskan pesan tersebut ke semua client yang terhubung. Ini memungkinkan setiap client untuk menerima dan melihat pesan yang dikirim oleh client lainnya.

Contoh interaksi yang terjadi adalah sebagai berikut: jika pengguna mengetikkan pesan di Client 1 dan mengirimkannya, pesan tersebut akan terlihat di terminal server sebagai penerima pesan. Server akan mengirimkan pesan tersebut kembali ke Client 1, Client 2, dan Client 3. Akibatnya, setiap client akan menerima pesan yang dikirim oleh client lainnya, dan pesan tersebut juga akan muncul di terminal server sebagai perantara komunikasi.

Dengan demikian, program ini memfasilitasi komunikasi antara client yang terhubung melalui server sebagai perantara. Pesan-pesan yang dikirim dari satu client akan diterima oleh semua client lainnya, memungkinkan interaksi dan pertukaran informasi antara pengguna yang menggunakan aplikasi ini.

## 2.2. Modifying the websocket port

![alt text](image-1.png)

Untuk menjalankan program, clone repositori dan jalankan server dengan cargo run --bin server. By default, server akan mendengarkan koneksi WebSocket pada port 2000. Jika ingin mengubah port server menjadi 8080, Anda dapat memodifikasi konfigurasi port dalam kode server sebelum melakukan kompilasi dan menjalankan ulang server. Selanjutnya, jalankan beberapa client dengan cargo run --bin client di terminal terpisah untuk menghubungkan ke server. Setelah semua client terhubung, Anda dapat berinteraksi dengan program chat dengan mengetik dan mengirim pesan di terminal client. Pesan yang dikirim akan diterima oleh semua client yang terhubung. Program ini memanfaatkan tokio_websockets untuk mengimplementasikan koneksi WebSocket secara asinkron di atas runtime Tokio. Jika tertarik berkontribusi, fork repositori ini dan ajukan perbaikan atau peningkatan melalui pull request.

