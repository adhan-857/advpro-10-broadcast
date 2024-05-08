# Tutorial Modul 10:  Asynchronous Programming
### Ramadhan Andika Putra (2206081976) - AdPro A <br>

**2.1. Original code of broadcast chat**<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/0108e543-1fb4-4503-a206-f54ff3ff395c)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/b59635e7-e3ef-498e-b93f-14bcd1b70a24)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/ff1e8144-bab9-49fa-9adb-597502b32a31)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/a10f46a1-cf6c-44b9-9a8f-db07ac09f755)<br>
Pada gambar, terlihat bahwa kita menjalankan sebuah server dan tiga buah *client*. Server dijalankan dengan menggunakan perintah `cargo run --bin server`, sementara *client* dijalankan dengan perintah `cargo run --bin client`. Saat salah satu *client* mengirimkan pesan ke server, maka pesan tersebut akan diteruskan atau di-*broadcast* ke semua *client* yang terkoneksi pada server yang sama. *Client* yang menerima pesan *broadcast* akan menerima pesan dengan pola ***"From server: {isi pesan}"***.