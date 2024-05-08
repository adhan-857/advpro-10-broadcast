# Tutorial Modul 10:  Asynchronous Programming
### Ramadhan Andika Putra (2206081976) - AdPro A <br>

**2.1. Original code of broadcast chat**<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/0108e543-1fb4-4503-a206-f54ff3ff395c)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/b59635e7-e3ef-498e-b93f-14bcd1b70a24)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/ff1e8144-bab9-49fa-9adb-597502b32a31)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/a10f46a1-cf6c-44b9-9a8f-db07ac09f755)<br>
Pada gambar, terlihat bahwa kita menjalankan sebuah server dan tiga buah *client*. Server dijalankan dengan menggunakan perintah `cargo run --bin server`, sementara *client* dijalankan dengan perintah `cargo run --bin client`. Saat salah satu *client* mengirimkan pesan ke server, maka pesan tersebut akan diteruskan atau di-*broadcast* ke semua *client* yang terkoneksi pada server yang sama. *Client* yang menerima pesan *broadcast* akan menerima pesan dengan pola ***"From server: {isi pesan}"***.
<br>
<br>
<br>

**2.2. Modifying the websocket port**
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/d1daa9e0-0e8e-437f-ae4b-43dfef33ccab)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/8be67265-93f8-4097-9513-3fdcb258176f)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/72c8b32a-b6bf-46d1-b0bc-10755ee46cbf)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/c70b52a1-7dad-462c-a7da-ce637afd1daa)<br>
Untuk percobaan pertama, akan dicoba *port* yang diubah adalah *port* untuk server dan *client* (sama-sama diubah menjadi 8080). Pada gambar diatas, terlihat dari *output* yang dihasilkan bahwa program tetap berjalan dengan normal seperti sebelumnya.
<br>
<br>

![image](https://github.com/adhan-857/tutorial-1/assets/119088782/c6e5f62a-1eda-45a0-9895-83160d5c63ba)<br>
![image](https://github.com/adhan-857/tutorial-1/assets/119088782/387f196d-017c-4925-904b-0ba089dd2c30)<br>
Sedangkan jika kita hanya mengganti *port* pada *client*, maka *port* pada client dan server berbeda dan akan menyebabkan *error* pada *client*. Hal ini karena tidak ada koneksi yang bisa dilakukan oleh *client* pada *websocket connection* yang telah ditetapkan. Sehingga program akan mengalami c*rash* seperti pada gambar.