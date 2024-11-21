## task day 3 cara koneksi dari server ke dbeaver

![ifconfig](/readme-md-day3/image/ifconfig.png);

pertama jalankan buka **vm virtual box manager** dan klik **ubuntu running** dan akan diarahkan di page seperti digambar, setelah itu kamu bisa ketikkan *ifconfig* ifconfig ini untuk bisa mengetahui ip address kalian untuk login di cmd

![login](/readme-md-day3/image/login.png);

setelah itu buka cmd dan **ssh user01@192.168.20.85** ingat 192 ip address saya, untuk bisa mengetahui ip addres yang kalian ifconfig tadi di ubuntu running yang ada tulisan inet tapi inet nya yang setelah docker nah itu ip addres nya, setelah itu login berhasil

![mkdir](/readme-md-day3/image/mkdir.png);

setelah itu buat directory baru dengan nama new_task_day3 kalau saya, direkctori sudah berhasil dibuat

![cd](/readme-md-day3/image/cd.png);

masukklah ke directory yang dibuat tadi dengan perintah **cd [nama directory baru]** kalau saya **cd new_task_day3**, dan berhasil masuk ke directory yang baru

![nano](/readme-md-day3/image/nano.png);

setelah itu buatlah docker-compose.yml dengan command **nano docker-compose.yml** 

![nano](/readme-md-day3/image/gnu-nano.png);

dan nanti akan diarahkan di GNU atau kepanjangan dari GNU's Not Unix, setelah itu saya mengetikkan code seperti digambar sesuai arahan mentor yaitu, membuat container name postgree_sql, maksimal connection 8000, buat selalu onboot, port 8785, time out connection 160 detik, ada pengecekan hell check, buat volume, gets dan block nya memory allocate 1 gb

### penjelasan apa itu docker-compose.yml

docker-compose.yml adalah file konfigurasi untuk docker compose, alat yang digunakan untuk mendefinisikan dan mengelola aplikasi berbasis docker yang terdiri dari beberapa container, file tersebut dituliskan dengan format YAML digunakan untuk mendeskripsikan layanan, jaringan dan volume yang dibutuhkan, terus juga bisa buat otomatisasi pengaturan container seperti port mapping, volume, dependencies antar layanan nya, dan yang terakhir membuat aplikasi lebih portable dan mudah direplikasi

### download postgresql

pertama klik ini https://www.enterprisedb.com/downloads/postgres-postgresql-downloads dan pilih versi 15 yang windows, setelah selesai download klik 2 kali file postgresql yang udah di download, untuk mengikuti langkah - langkah boleh klik link ini https://www.enterprisedb.com/postgres-tutorials/postgres-installer-step-step-guide-install-postgresql, setelah itu kalian bisa cek apakah postgresql sudah di instal dengan command **postgres --version** di cmd kalian tapi sesuai penempatan foldernya biasanya sih di C:\Program Files\PostgreSQL\15\bin> default nya

### cara connect server dengan dbeaver

![db1](/readme-md-day3/image/connect-db1.png);

masuk ke dbeaver dan klik button seperti digambar di pojok kiri, dan akan muncul page seperti gambar dibawah

![db2](/readme-md-day3/image/connect-db2.png);

pilih yang PostgreSQL, setelah itu next, dan muncul page seperti gambar bawah

![db3](/readme-md-day3/image/connect-db3.png);

disitu ada field host, ganti localhost dengan ip address yaitu 192.168.20.85 dan port nya 8785 sesuai mentor kalian dan password nya isi **postgres** setelah itu click finish

![db4](/readme-md-day3/image/connect-db4.png);

setelah itu cek, kalau misalkan sudah ada centang hijau menandakan bahwa koneksi antara server dan dbeaver sudah berhasil

### apa itu volumes di docker compose

volumes adalah mekanisme untuk menyimpan data yang dihasilkan dan digunakan oleh container docker, volumes untuk membuat data tetap ada meskipun container dihapus atau dihentikan, berguna untuk menyimpan data file database, file konfigurasi, atau data lainnya, contohnya 

![volumes](/readme-md-day3/image/volumes.png);

yang saya buat seperti gambar diatas, **pgdata** digunakan untuk menyimpan data dari PostgreSql,ini mendeklarasikan volume bernama pgdata dengan driver local. Driver local adalah driver default yang menyimpan data di sistem file host. jadi semua data yang disimpan oleh PostgreSQL akan disimpan di volume pgdata di host, ini memastikan bahwa data tetap ada meskipun dihentikan atau dihapus.

![volume](/readme-md-day3/image/volume.png);

untuk melihat volume pakai command **docker volume list** dan akan muncul list volume nya


### volume

![volume](/readme-md-day3/image/volume1.png);

volumes pgdata untuk menyimpan data dari PostgreSQL, semua data akan disimpan di volume pgdata nya
