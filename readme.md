# step tasks devops


![ubah hostname dengan nama MyServer](images/ubah_hostname.png)

pertama ubah hostname dengan nama MyServer

![ubah hostname dengan nama MyServer](images/make-sure-open-ssh.png)

kedua saya make sure open ssh will be started on boot

![generate ssh key pair](images/generate-ssh-key-pair.png)

ketiga saya generate ssh with key pair

![login server tanpa password](images/login-MyServer-tanpa-password.png)

keempat coba login MyServer tanpa password

# penjelasan cara kerja ssh

SSH Key-Pair mempunyai 2 yaitu :
- private key = disimpan dikomputer lokal
- public key = ditempatkan diserver

# copy some files/directories using SCP and RSYNC

![copy some files](images/copy-some-files.png)

# membuat ssh local (private_key)

![membuat ssh local](images/private-in-local.png)

# show ssh local (private_key)

![membuat ssh local](images/show-ssh-private-local.png)

 - user01@MyServer:~/only-office$ logout
Connection to 192.168.20.79 closed.
PS C:\Users\LAWENCON>

command diata adalah untuk logout dari server

- PS C:\Users\LAWENCON> ssh user01@192.168.20.79

command ini digunakan untuk login server, yaitu servernya 192.168.20.79

- user01@MyServer:~$ pwd

untuk mengetahui posisi kita lagi dimana

- user01@MyServer:~$ ls

untuk menampilkan isi file dan direktori

- user01@MyServer:~$ cd only-office

command ini untuk berpindah ke direktori lain

- user01@MyServer:~/only-office$ mkdir app

untuk membuat direktori baru di direktori only-office

- user01@MyServer:~/only-office$ cat docker-compose.yml

untuk menampilkan isi content docker-compose.yml

- user01@MyServer:~/only-office$ nano docker-compose.yml

untuk mengedit isi content dari docker-compose.yml

- user01@MyServer:~/only-office$ rm docker-compose.yml

untuk menghapus direktori/file

![nano docker compose](images/nano-docker-compose.png)

jadi ports:
      - "2678:80"

- port 80 = adalah port internal yang digunakan nginx di dalam container
- port 2678 = adalah port host nya yang kita buat di docker.compose.yml



**user01@MyServer:~/only-office$ docker-compose up -d** =
command ini untuk running docker compose

![container yang jalan](images/container-yang-jalan.png)

command untuk melihat container apa aja yang jalan