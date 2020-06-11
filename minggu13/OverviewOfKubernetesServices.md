Kubernetes Pods adalah fana. Polong sebenarnya memiliki siklus hidup. Ketika node pekerja mati, Pod yang berjalan di Node juga hilang. Sebuah ReplicaSet mungkin kemudian secara dinamis mengarahkan kluster kembali ke keadaan yang diinginkan melalui pembuatan Pods baru untuk menjaga aplikasi Anda tetap berjalan. Sebagai contoh lain, pertimbangkan backend pemrosesan gambar dengan 3 replika. Replika itu dapat ditukar; sistem front-end seharusnya tidak peduli tentang replika backend atau bahkan jika Pod hilang dan diciptakan kembali. Yang mengatakan, setiap Pod di kluster Kubernetes memiliki alamat IP yang unik, bahkan Pods pada Node yang sama, sehingga perlu ada cara untuk secara otomatis merekonsiliasi perubahan di antara Pod sehingga aplikasi Anda terus berfungsi.

Layanan di Kubernetes adalah abstraksi yang mendefinisikan kumpulan logis Pods dan kebijakan yang digunakan untuk mengaksesnya. Layanan memungkinkan sambungan longgar antara Pods dependen. Layanan didefinisikan menggunakan YAML (lebih disukai) atau JSON, seperti semua objek Kubernetes. Set Pods yang ditargetkan oleh Layanan biasanya ditentukan oleh LabelSelector (lihat di bawah untuk alasan Anda mungkin menginginkan Layanan tanpa menyertakan pemilih dalam spesifikasi).

Meskipun setiap Pod memiliki alamat IP yang unik, IP tersebut tidak diekspos di luar cluster tanpa Layanan. Layanan memungkinkan aplikasi Anda menerima lalu lintas. Layanan dapat diekspos dengan berbagai cara dengan menentukan jenis di ServiceSpec:

ClusterIP (default) - Mengekspos Layanan pada IP internal di cluster. Jenis ini membuat Layanan hanya dapat dijangkau dari dalam kluster.
NodePort - Mengekspos Layanan pada port yang sama dari setiap Node yang dipilih dalam cluster menggunakan NAT. Membuat Layanan dapat diakses dari luar cluster menggunakan <NodeIP>: <NodePort>. Superset dari ClusterIP.
LoadBalancer - Membuat penyeimbang beban eksternal di cloud saat ini (jika didukung) dan menetapkan IP eksternal tetap ke Layanan. Superset dari NodePort.
ExternalName - Mengekspos Layanan menggunakan nama arbitrer (ditentukan oleh externalName dalam spesifikasi) dengan mengembalikan catatan CNAME dengan nama tersebut. Tidak ada proxy yang digunakan. Tipe ini membutuhkan v1.7 atau lebih tinggi dari kube-dns.
Informasi lebih lanjut tentang berbagai jenis Layanan dapat ditemukan di tutorial Menggunakan Sumber IP. Juga lihat Menghubungkan Aplikasi dengan Layanan.

Selain itu, perhatikan bahwa ada beberapa kasus penggunaan dengan Layanan yang melibatkan tidak menentukan pemilih dalam spesifikasi. Layanan yang dibuat tanpa pemilih juga tidak akan membuat objek Endpoint yang sesuai. Ini memungkinkan pengguna untuk memetakan Layanan secara manual ke titik akhir tertentu. Kemungkinan lain mengapa tidak ada pemilih adalah Anda hanya menggunakan tipe: ExternalName.

Ringkasan
Memaparkan Pods ke lalu lintas eksternal
Muat penyeimbangan lalu lintas di beberapa Pod
Menggunakan label
Layanan Kubernetes adalah lapisan abstraksi yang mendefinisikan kumpulan logis Pods dan memungkinkan pemaparan lalu lintas eksternal, penyeimbangan muatan, dan penemuan layanan untuk Pods tersebut.

Layanan merutekan lalu lintas melintasi satu set Pod. Layanan adalah abstraksi yang memungkinkan pod untuk mati dan bereplikasi di Kubernetes tanpa memengaruhi aplikasi Anda. Penemuan dan perutean di antara Pods dependen (seperti komponen frontend dan backend dalam aplikasi) ditangani oleh Kubernetes Services.

Layanan cocok dengan serangkaian Pod menggunakan label dan pemilih, primitif pengelompokan yang memungkinkan operasi logis pada objek di Kubernetes. Label adalah pasangan kunci / nilai yang melekat pada objek dan dapat digunakan dengan berbagai cara:

Tentukan objek untuk pengembangan, pengujian, dan produksi
Sematkan tag versi
Klasifikasi objek menggunakan tag

Label dapat dilampirkan ke objek pada saat pembuatan atau nanti. Mereka dapat dimodifikasi kapan saja.