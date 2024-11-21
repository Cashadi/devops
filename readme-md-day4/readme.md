# task day 4 (deploy apps)

![buat direktori baru](/readme-md-day4/images/mkdir.png);

pertama buat direktori terlebih dahulu, kalau saya nama nya **task_day4**

![cd](/readme-md-day4/images/cd.png);

kedua masuk ke direktori nya dengan command **cd**

![cd](/readme-md-day4/images/mkdir-apps.png);

ketiga buat direktori baru tapi di dalam direktori **task_day4** biasa dengan command **cd apps**

keempat masuk kedirektori apps nya, dan buat index.html dengan command **index.html** 

![nano](/readme-md-day4/images/index-html.png);

enter lalu masuk ke tampilan GNU masukkan kode html yang sudah disiapkan untuk dideploy

![nano](/readme-md-day4/images/html-code.png);

save dan exit, kelima buat direktori baru dengan nama css, seperti biasa command **mkdir css** 

![nano](/readme-md-day4/images/css.png);

masuk ke direktori css dan buat index.css dengan command **nano index.css**, dan akan ke tampilan GNU seperti biasa masukkan code css nya yang sudah disiapkan dan save dan exit 

![nano](/readme-md-day4/images/gnu-css.png);

keluar dari direktori css dengan command **cd ../**, command itu memberi perintah untuk mundur 1 langkah 

![nano](/readme-md-day4/images/kembali-apps.png);

dan akan kembali ke direktori apps setlah itu masukkan asset, kan asset saya ada banyak dalam folder dalam folder gitu, tadi saya cari cara dengan melakukan command seperti gambar bawah

![nano](/readme-md-day4/images/scp.png);

itu saya menyalin direktori assets dari local ke server ubuntu menggunakan SCP (Secure Copy Protocol)

dan yah berhasil, setelah itu ke direktori apps dengan command **cd ../** untuk mundur 1 langkah

terus buat docker-compose.yml dengan command **nano docker-compose.yml** dan akan ke tampilan GNU dan saya ketik code seperti ini

![nano](/readme-md-day4/images/docker-compose-apps.png);

saya menggunakan port 2202 untuk bisa akses ke web nya, dan digambar ada letak volumes, setelah membuat docker-compose.yml buat nginx.conf

dengan command **nano nginx.conf**, dan isi code berikut

![nano](/readme-md-day4/images/conf-apps.png);

di location kedua saya menambahkan seperti format buat ngebaca gambar nya dan **autoindex on** 
Fungsi autoindex on dalam konfigurasi Nginx adalah untuk menampilkan daftar file dalam direktori ketika tidak ada file indeks (index.html) yang ditemukan di dalam folder tersebut.

setelah itu command **docker-compose up -d** untuk running docker nya 

![nano](/readme-md-day4/images/up.png);

setelah itu cek di browser dan ketik **192.168.20.85:2202** di browser dan boom web bisa diakses

![nano](/readme-md-day4/images/web.png)





