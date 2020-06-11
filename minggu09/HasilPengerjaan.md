Docker untuk Pemula - Linux


Tugas 1: Jalankan beberapa wadah Docker sederhana

1. Jalankan satu tugas dalam wadah Alpine Linux

- Jalankan perintah berikut di konsol Linux Anda.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar1.JPG

- Docker menjaga wadah berjalan selama proses itu dimulai di dalam wadah masih berjalan. Dalam hal ini proses nama host keluar segera setelah output ditulis. Ini artinya wadah berhenti. 
Namun, Docker tidak menghapus sumber daya secara default, sehingga wadah masih ada dalam status Keluar.

Daftar semua wadah.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar2.JPG


2. Jalankan wadah Ubuntu interaktif

- Jalankan wadah Docker dan akses cangkangnya.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar3.JPG

- Jalankan perintah berikut dalam wadah.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar4.JPG

- Ketik exit untuk keluar dari sesi shell. Ini akan menghentikan proses bash, menyebabkan wadah untuk keluar.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar5.JPG

- Untuk bersenang-senang, mari kita periksa versi VM host kami.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar6.JPG


3. Jalankan latar belakang wadah MySQL

- Jalankan wadah MySQL baru dengan perintah berikut.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar7.JPG

- Daftar wadah yang sedang berjalan.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar8.JPG

- Anda dapat memeriksa apa yang terjadi di wadah Anda dengan menggunakan beberapa perintah Docker bawaan: log kontainer buruh pelabuhan dan bagian atas wadah buruh pelabuhan.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar9.JPG

Mari kita lihat proses yang berjalan di dalam wadah.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar10.JPG

- Daftar versi MySQL menggunakan exec kontainer buruh pelabuhan.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar11.JPG

- Anda juga dapat menggunakan exec kontainer galangan untuk terhubung ke proses shell baru di dalam wadah yang sudah berjalan. Menjalankan perintah di bawah ini akan memberi Anda shell interaktif (sh) di dalam wadah MySQL Anda.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu09/gambar12.JPG
