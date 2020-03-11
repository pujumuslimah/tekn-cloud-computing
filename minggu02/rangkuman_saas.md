
1.	Perbedaan IaaS, PaaS dan SaaS

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu02/gambar1.jpg

IaaS PaaS & SaaS   adalah tiga model komputasi Cloud 

a.	IaaS(Infra sebagai layanan)
IaaS menyediakan infrastruktur seperti mesin virtual dan sumber daya lain seperti perpustakaan citra 
disk mesin-virtual, blok dan penyimpanan berbasis file, firewall, penyeimbang muatan, alamat IP, 
jaringan area lokal virtual, dll. Infrastruktur sebagai layanan atau IaaS adalah lapisan dasar 
dalam model komputasi awan. Contoh umum: DigitalOcean, Linode, Rackspace, Amazon Web Services (AWS), 
Cisco Metapod, Microsoft Azure, Google Compute Engine (GCE) adalah beberapa contoh populer Iaas.

b.	PaaS (Platform sebagai layanan)
PaaS atau platform sebagai model layanan memberi Anda platform komputasi yang biasanya mencakup 
sistem operasi, lingkungan eksekusi bahasa pemrograman, database, server web. secara teknis Ini adalah 
lapisan di atas IaaS sebagai hal kedua yang Anda minta setelah Infrastruktur adalah platform. 
Yaitu , komputer yang Anda dapatkan dalam penawaran PaaS, memiliki OS dan tumpukan perangkat 
lunak yang tetap. Anda dapat menjalankan perangkat lunak Anda di atas ini. Contoh, Anda dapat 
menggunakan kode apa pun di atas mesin aplikasi Google. Contoh umum: AWS Elastic Beanstalk, Windows 
Azure, Heroku, tenaga penjualan, Google App Engine, Apache Stratos.


c.	SaaS (Perangkat Lunak sebagai layanan)
Dalam SaaS Anda diberikan akses ke layanan aplikasi yang diinstal di server. 
Anda tidak perlu khawatir tentang instalasi, pemeliharaan, atau pengkodean perangkat lunak itu. 
Anda dapat mengakses dan mengoperasikan perangkat lunak hanya dengan browser Anda. Anda tidak perlu m
engunduh atau menginstal segala jenis pengaturan atau OS, perangkat lunak ini hanya tersedia untuk 
Anda akses dan operasikan. Pemeliharaan atau pengaturan atau bantuan perangkat lunak akan diberikan 
oleh perusahaan penyedia SaaS dan Anda hanya perlu membayar untuk penggunaan Anda. 
yaitu, Anda menggunakan perangkat lunak yang tersedia online, dan hanya itu. 
Contoh umum: Google Apps, Microsoft office365, Google docs, Gmail, perangkat lunak penagihan WHMCS

Perbedaan antara IaaS PaaS & SaaS

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu02/gambar2.jpg

Referensi
https://www.quora.com/What-is-the-difference-between-IaaS-SaaS-and-Paas


2.	Arsitektur Platform SAAS (Perangkat Lunak sebagai Layanan)
Perangkat lunak sebagai layanan adalah model lisensi dan pengiriman perangkat lunak di mana perangkat
lunak dilisensikan berdasarkan berlangganan dan di-host secara terpusat. 
Pengguna dapat mengaksesnya dengan bantuan browser web. SaaS adalah model pengiriman umum untuk
banyak aplikasi bisnis, termasuk perangkat lunak perkantoran dan pesan, perangkat lunak manajemen, 
virtualisasi dll. Ini adalah bagian dari nomenklatur komputasi awan, bersama dengan infrastruktur 
sebagai layanan (IaaS), platform sebagai layanan (PaaS) , desktop sebagai layanan (DaaS). 
Selama transmisi dan penyimpanan 

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu02/gambar3.jpg

Arsitektur SAAS:
Dengan model ini, satu versi aplikasi, dengan satu konfigurasi digunakan untuk semua pelanggan. 
Aplikasi ini diinstal pada banyak mesin untuk mendukung skalabilitas (disebut penskalaan horizontal). 
Dalam beberapa kasus, versi kedua aplikasi diatur untuk menawarkan kelompok pelanggan tertentu dengan 
akses ke versi pra-rilis aplikasi untuk tujuan pengujian. Dalam model tradisional ini, 
setiap versi aplikasi didasarkan pada kode unik. Meskipun pengecualian, beberapa solusi SaaS tidak 
menggunakan multitenancy, untuk mengelola secara efektif sejumlah besar pelanggan di tempat. 
Apakah multitenancy merupakan komponen yang diperlukan untuk perangkat lunak-sebagai-layanan adalah 
topik kontroversi.

•	SaaS Vertikal
Perangkat Lunak yang menjawab kebutuhan industri tertentu (mis. Perangkat lunak untuk kesehatan, 
pertanian, real estat, industri keuangan)

•	SaaS Horisontal
Produk-produk yang berfokus pada kategori perangkat lunak (pemasaran, penjualan, alat pengembang, SDM)tetapi agnostik industri.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu02/gambar4.jpg
 
Manfaat SAAS:
Ini menawarkan peluang besar bagi organisasi dari semua ukuran untuk mengalihkan risiko akuisisi 
perangkat lunak, dan untuk memindahkan TI dari pusat biaya reaktif menjadi bagian perusahaan yang 
proaktif dan bernilai tambah. Secara tradisional, menyebarkan sistem perangkat lunak skala besar 
telah menjadi tugas utama. Menyebarkan sistem ini di perusahaan besar membutuhkan biaya lebih besar. 
Waktu, staf, dan persyaratan anggaran untuk penyebaran sebesar ini mewakili risiko yang signifikan 
bagi organisasi dalam ukuran berapa pun, dan sering kali menempatkan perangkat lunak seperti itu di 
luar jangkauan organisasi yang lebih kecil yang jika tidak dapat diturunkan darinya banyak utilitas. 
Model pengiriman berdasarkan permintaan mengubah beberapa hal ini. Aplikasi SaaS tidak memerlukan 
penyebaran infrastruktur besar di lokasi klien.

Bagaimana SaaS Mempengaruhi IT?
Setelah Anda membuat keputusan untuk mengejar SaaS, langkah selanjutnya adalah mempersiapkan transisi 
dengan menilai bagaimana penyebaran akan mempengaruhi aset TI yang ada. Melakukan uji tuntas adalah 
bagian rutin dari setiap proyek penyebaran infrastruktur TI yang sukses. Beberapa bidang yang harus 
ditangani dalam daftar periksa uji tuntas meliputi, Standar keamanan data: Memindahkan data bisnis 
penting "di luar tembok" menimbulkan risiko kehilangan data atau paparan informasi sensitif yang tidak disengaja.
Dampak pada Peran dan Tanggung Jawab TI Menambahkan SaaS dapat menyebabkan perubahan mendasar dalam peran departemen 
TI sebagai penyedia layanan informasi. Di masa lalu, sifat penyebaran perangkat lunak telah menempatkan petugas informasi kepala 
dalam peran penjaga gerbang. Mereka dapat melakukan veto dengan menyatakan bahwa mereka tidak akan meng-host-nya di pusat data. 
Dengan SaaS, kontrol pusat data tidak harus sama dengan kontrol atas seluruh lingkungan komputasi perusahaan. 
Ini dapat menyebabkan penjaga gerbang takut kehilangan kendali.

Referensi :
1. https://en.wikipedia.org/wiki/Software_as_a_service
2. https://msdn.microsoft.com/en-us/library/aa905332.aspx
3. https://hackernoon.com/saas-software-as-a-service-platform-architecture-757a432270f5


3.	Arsitektur Platform SAAS (Perangkat Lunak sebagai Layanan)
Apa itu Platform SaaS?
SaaS adalah cara untuk mengirimkan perangkat lunak, penyedia perangkat lunak ini secara sentral menampung satu atau 
lebih aplikasi dan membuatnya tersedia bagi pelanggan melalui internet.
Setiap pembaruan atau tambalan untuk aplikasi SaaS semuanya ditangani oleh penyedia. 
Pelanggan tidak perlu mengunduh pemutakhiran atau menginstal ulang versi baru suatu produk 
saat perangkat lunak dikirimkan melalui internet.

Mengapa Menggunakan Arsitektur SaaS?

Dari perspektif konsumen, produk SaaS adalah salah satu cara termudah untuk menggunakan layanan atau produk digital. 
Anda cukup mengaksesnya melalui web, membayar layanan dan menggunakannya! Dalam beberapa tahun terakhir kita telah 
melihat munculnya ribuan produk SaaS yang ditargetkan untuk konsumen seperti: Netflix, Microsoft Office 365, Amazon Prime, 
Indonesia, Facebook, Google Documents, dll. Dari perspektif bisnis, produk perangkat lunak yang dikirimkan “sebagai layanan” 
memungkinkan perusahaan untuk menawarkan produk mereka dalam skala global, sementara juga memungkinkan mereka untuk 
mempertahankan kontrol keseluruhan atas produk mereka. Beberapa manfaat lain dari penerapan arsitektur SaaS dalam bisnis termasuk, 
tetapi tidak terbatas pada: Mengurangi waktu ke pasar, Biaya perawatan lebih rendah, Pembaruan yang lebih mudah.

Fitur dan Manfaat Utama dari Platform SaaS
beberapa manfaat lain yang dapat diberikan oleh penggunaan produk berbasis SaaS.
1.	Kesederhanaan
2.	Ekonomis
3.	Keamanan
4.	Kesesuaian

Kemampuan Solusi SaaS

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu02/gambar5.jpg

Teknologi cloud seperti Microsoft Azure memungkinkan Anda menyediakan server yang dapat meng-host situs web, database, dan banyak lagi. 
Infrastruktur yang secara historis akan secara fisik dipasang di tempat bisnis dan dijalankan oleh tim TI internal, sekarang dapat disediakan 
dari dasbor online hanya dengan beberapa klik mouse. Solusi SaaS dapat digunakan untuk lingkungan ini dan, secara teori, menawarkan semua jenis 
layanan yang dapat dikembangkan sebagai aplikasi perangkat lunak yang dapat mencakup, tetapi tidak terbatas pada:
•	Aplikasi kantor
•	Email dan pesan instan
•	Media sosial
•	Mengekspos 3 rd  API Partai
•	Keamanan dan otentikasi
•	Pembelajaran mesin
•	Kecerdasan buatan
•	Layanan Lokasi
•	Streaming data dan layanan pencarian

Kerugian dari Platform SaaS
1.	Kurang control
2.	Ekosistem terbatas
3.	Performa
4.	Kekhawatiran Data

Komponen Kunci dari Platform SaaS

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu02/gambar6.jpg

4.Cara membangun aplikasi SaaS berbasis cloud

Bangun untuk cloud
Saat membangun aplikasi SaaS (global), kemungkinan besar Anda membangunnya di cloud. The awan memiliki banyak keuntungan 
- memikirkan skalabilitas 
- kontras dengan lingkungan server lokal.

Bagaimana cara memulai?ssssssss
Beberapa pertanyaan untuk memulai :
1.	Bahasa pemrograman mana?
2.	Basis data yang sempurna
3.	MongoDB - database untuk aplikasi web Anda?


referensi : https://usersnap.com/blog/cloud-based-saas-architecture-fundamentals/




