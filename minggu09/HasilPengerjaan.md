Docker untuk Pemula - Linux


Tugas 1: Jalankan beberapa wadah Docker sederhana

1. Jalankan satu tugas dalam wadah Alpine Linux

- Jalankan perintah berikut di konsol Linux Anda.
gb1

- Docker menjaga wadah berjalan selama proses itu dimulai di dalam wadah masih berjalan. Dalam hal ini proses nama host keluar segera setelah output ditulis. Ini artinya wadah berhenti. 
Namun, Docker tidak menghapus sumber daya secara default, sehingga wadah masih ada dalam status Keluar.

Daftar semua wadah.

gb2


2. Jalankan wadah Ubuntu interaktif

- Jalankan wadah Docker dan akses cangkangnya.

gb3

- Jalankan perintah berikut dalam wadah.

gb4

- Ketik exit untuk keluar dari sesi shell. Ini akan menghentikan proses bash, menyebabkan wadah untuk keluar.

gb5

- Untuk bersenang-senang, mari kita periksa versi VM host kami.

gb6


3. Jalankan latar belakang wadah MySQL

- Jalankan wadah MySQL baru dengan perintah berikut.

gb7 

- Daftar wadah yang sedang berjalan.

gb8

- Anda dapat memeriksa apa yang terjadi di wadah Anda dengan menggunakan beberapa perintah Docker bawaan: log kontainer buruh pelabuhan dan bagian atas wadah buruh pelabuhan.

gb9

Mari kita lihat proses yang berjalan di dalam wadah.

gb10

- Daftar versi MySQL menggunakan exec kontainer buruh pelabuhan.

gb11

- Anda juga dapat menggunakan exec kontainer galangan untuk terhubung ke proses shell baru di dalam wadah yang sudah berjalan. Menjalankan perintah di bawah ini akan memberi Anda shell interaktif (sh) di dalam wadah MySQL Anda.

gb12

- Mari kita periksa nomor versi dengan menjalankan perintah yang sama lagi, hanya kali ini dari dalam sesi shell baru di wadah.

gb13