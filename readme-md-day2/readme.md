## command login

![login](/images/login.png);

untuk bisa login ke server bisa menggunakan command ssh namaUser@api nya, contohnya saya menggunakan **ssh user01@192.168.20.79**, nah Ip Addres itu dapet dari mana sih?, Ip Address tersebut didapatkan dari ubuntu kalian ketika running, ketika sukses login di paling bawah ada teks yang menginfokan bahwa kamu login di waktu tersebut


## command logout

![ubah hostname dengan nama MyServer](/images/logout.png);

untuk logout dari server bisa mengetikkan kata **logout** dan akan menghasilkan output *Connection to 192.168.20.79 closed.*

## command pwd (Print Working Directory)

![pwd](/images/pwd.png);

command pwd adalah untuk mengetahui kita berada di direktori mana, contoh seperti digambar ketika saya ketik pwd akan muncul di direktori mana saya berada yaitu di user01

## command ls (List Directory)

![ls](/images/ls.png);

pernah ngerasa bingung direktori/file apa aja sih yang didalamnya, untuk mengetahui isi dari direktori kalian bisa command **ls** dan enter, nah nanti output nya direktori/file yang di direktori yang kalian berada

## command cd (Change Directory)

![ls](/images/cd.png);

nah untuk berpindah ke direktori lain kalian bisa masukkan **cd [nama direktori]**, contohnya seperti di gambar saya ingin berpindah ke direktori only-office ya tinggal ketik **cd only-office**, tapi ingat hanya *text yang berwarna biru* karena folder yang mempunyai direktori lagi, kalau ke *initest2.txt* nggk bisa karena itu bukan folder, jadi hanya **text berwarna biru yang bisa cd**

## command mkdir (Make Directory)

![mkdir](/images/mkdir.png);

untuk membuat sebuah direktori baru bisa menggunakan **mkdir**, contoh nya seperti digambar saya buat **mkdir new** nanti akan kebuat direktori dengan nama new, dan ketika ls kenapa new itu berwarna biru?, karena dia sebuah folder jadi kita bisa cd ke new

## command cat (concatenate)

![cat](/images/cat.png);

untuk bisa tahu isi dari sebuat file txt atau yang lainnya pakai lah **cat** ini untuk menampilkan, membaca, dan menggabungkan berkas teks

## command nano (concatenate)

![cat](/images/nano.png);

apakah kalian ingin mengedit teks?, untuk bisa mengedit teks di dalam cmd kalian bisa ketikkan **nano** ketika enter nanti akan tampil seperti ini

![cat](/images/tampilan-gnu.png);

disini bisa edit teks nya, tapi disini tidak bisa menggunakan cursor hanya bisa menggunakan tombol kiri, kanan, bawah, atas di tombol laptop kalian, dan dibawah itu ada perintah - perintah untuk gunakan di GNU itu

## command rm (remove)

![rm](/images/rm.png);

untuk menghapus direktori atau berkas teks kalian bisa menggunakan command **rm [nama direktori]** dan enter, contoh digambar saya akan hapus *initest2.txt* dan ketika saya ls *initest2.txt* sudah terhapus

## command docker-compose up -d (running docker)

![rm](/images/running.png);

untuk bisa menjalankan docker compose yang kita buat ketik command **docker-compose up -d** dan enter dia akan menjalan docker compose yang kita buat, terus kita bisa cek hasilnya di browser dengan port yang kita setting di *docker-compose.yml* nya 

![rm](/images/gnu-docker-compose.png);

gambar diatas adalah port yang saya buat yaitu **2678:80**. 
- port 80 = adalah port internal yang digunakan nginx di dalam container
- port 2678 = adalah port host nya yang kita buat di docker.compose.yml

nah untuk melihat hasilnya kita masukkin aja **[api server yang dibuat] [port yang dibuat di docker.compose.yml]** kalau saya pakai *http://192.168.20.79:2678/*

## buat docker.compose.yml (running docker)

![rm](/images/docker-compose-yml.png);

untuk membuat docker.compose.yml kalian bisa gunakan **nano docker.compose.yml** dan akan diarahkan ke gnu

![rm](/images/gnu-docker-compose%20(2).png);

dan disitu kalian masukkan code 

![rm](/images/new-docker-compile.png);

nah disitu ada port, port tersebut masukkan apa yang disuruh oleh mentor mu, setelah itu **docker.compose.yml** berhasil di buat

## buat nginx.conf

seperti biasa tulis **nano nginx.conf** dan kalian akan diarahkan ke gnu, dan tulis code 

![rm](/images/gnu-nginx-conf.png);

setelah itu save **ctrl + s** dan exit, kita sudah membuat docker.compose.yml dan nginx.conf nya 

jalan kan perintah dengan command 

- **docker-compose down** untuk merestart agar perubahan di terapkan, setelah itu
- **docker-compose up -d** untuk running docker nya

setelah itu cek browser *http://192.168.20.79:2678/*, maka akan tampil

![rm](/images/result-browser.png);
