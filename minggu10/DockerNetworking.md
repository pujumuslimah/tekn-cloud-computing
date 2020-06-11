Docker Networking Hands-on Lab

Bagian # 1 - Dasar-Dasar Jaringan

1. Perintah Jaringan Docker

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar1.JPG

2. Daftar jaringan

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar2.JPG

3. Periksa jaringan

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar3.JPG

4. Daftar plugin driver jaringan

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar4.JPG

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar5.JPG



Bagian # 2 - Jembatan Jaringan

1. Dasar-Dasarnya
Setiap instalasi Docker yang bersih dilengkapi dengan jaringan yang disebut jembatan. Verifikasi ini dengan jaringan buruh pelabuhan ls.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar6.JPG

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar7.JPG

2. Hubungkan sebuah wadah

Buat wadah baru dengan menjalankan docker run -dt ubuntu sleep infinity.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar8.JPG

Perintah ini akan membuat wadah baru berdasarkan ubuntu: gambar terbaru dan akan menjalankan perintah tidur untuk menjaga wadah tetap berjalan di latar belakang. Anda dapat memverifikasi wadah contoh kami sudah habis dengan menjalankan buruh pelabuhan ps.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar9.JPG

Jalankan perintah show brctl lagi.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar10.JPG

Anda dapat memeriksa jaringan jembatan lagi, dengan menjalankan jaringan buruh pelabuhan memeriksa jembatan, untuk melihat wadah baru yang melekat padanya.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar11.JPG

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar12.JPG


3. Uji konektivitas jaringan

Pertama, kita perlu mendapatkan ID wadah dimulai pada langkah sebelumnya. Anda dapat menjalankan buruh pelabuhan ps untuk mendapatkan itu.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar13.JPG

4. Konfigurasikan NAT untuk konektivitas eksternal

Mulai wadah baru berdasarkan gambar NGINX resmi dengan menjalankan docker run --name web1 -d -p 8080: 80 nginx.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar14.JPG

Tinjau status kontainer dan pemetaan port dengan menjalankan docker ps.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar15.JPG

Jika karena alasan tertentu Anda tidak dapat membuka sesi dari web broswer, Anda dapat terhubung dari host Docker Anda menggunakan perintah curl 127.0.0.1:8080.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar16.JPG



Bagian # 3 - Overlay Networking

1. Dasar

Jalankan docker swarm init --advertise-addr $ (hostname -i).

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar17.JPG

Jalankan node docker ls untuk memverifikasi bahwa kedua node adalah bagian dari Swarm.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar18.JPG

2. Buat jaringan hamparan

Buat jaringan overlay baru yang disebut "overnet" dengan menjalankan docker network create -d overlay overnet

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar19.JPG

Gunakan perintah docker network ls untuk memverifikasi bahwa jaringan berhasil dibuat.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar20.JPG

Jalankan perintah docker network ls yang sama dari terminal kedua.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar21.JPG

Gunakan jaringan buruh pelabuhan periksa perintah <network> untuk melihat informasi lebih rinci tentang jaringan "overnet". Anda perlu menjalankan perintah ini dari terminal pertama.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar22.JPG

3. Buat layanan

Jalankan perintah berikut dari terminal pertama untuk membuat layanan baru yang disebut myservice pada jaringan overnet dengan dua tugas / replika.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar23.JPG

Verifikasi bahwa layanan dibuat dan kedua replika sudah aktif dengan menjalankan layanan buruh pelabuhan ls.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar24.JPG

Verifikasi bahwa satu tugas (replika) berjalan di masing-masing dari dua node di Swarm dengan menjalankan layanan buruh pelabuhan dan layanan saya.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar25.JPG

Sekarang simpul kedua menjalankan tugas pada jaringan "overnet", ia akan dapat melihat jaringan "overnet". Mari kita jalankan jaringan buruh pelabuhan dari terminal kedua untuk memverifikasi ini.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar26.JPG

Kami juga dapat menjalankan jaringan buruh pelabuhan memeriksa overnet pada terminal kedua untuk mendapatkan informasi lebih rinci tentang jaringan "overnet" dan mendapatkan alamat IP dari tugas yang berjalan pada terminal kedua.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar27.JPG

4. Uji jaringan

Jalankan perintah berikut dari terminal pertama.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar28.JPG

Jalankan perintah buruh pelabuhan ps untuk mendapatkan ID tugas layanan sehingga Anda bisa masuk ke dalamnya di langkah berikutnya.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar29.JPG

instal perintah ping dan ping tugas layanan yang berjalan pada node kedua di mana ia memiliki alamat IP 10.0.0.3 dari jaringan buruh pelabuhan memeriksa perintah overnet.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar30.JPG

5. Uji penemuan layanan

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar31.JPG


Cleaning Up

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu10/gambar32.JPG