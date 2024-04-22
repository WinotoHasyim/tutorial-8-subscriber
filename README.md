## What is amqp?

AMQP (Advanced Message Queuing Protocol) adalah sebuah open standard protocol untuk message-oriented middleware. AMQP memungkinkan komunikasi pesan yang handal dan aman antara komponen sistem yang berbeda. AMQP dalam main.rs di direktori ini bertujuan untuk memfasilitasi komunikasi antara aplikasi dan message broker.

## guest:guest@localhost:5672 , what is the first quest, and what is the second guest, and what is localhost:5672 is for? 

guest:guest@localhost:5672 digunakan untuk menghubungkan message broker dengan AMQP Protocol. guest pertama adalah username dan guest kedua adalah password. localhost:5672 adalah hostname dan port number dimana aplikasi mencoba untuk terhubung dengan message broker seperti RabbitMQ.

## Simulation slow subscriber

![Simulation slow subscriber](https://i.imgur.com/4VDwwqX.png)

Bisa dilihat bahwa pada gambar tersebut total queued message adalah 20 karena saya menjalankan command cargo run sebanyak 5 kali. Message yang diqueue disebabkan oleh subscriber yang lambat dalam memproses message (delay 1 detik) sehingga message akan ditampilkan di subscriber secara perlahan-lahan seperti yang ditunjukkan oleh garis ungu dalam gambar