Saat Anda membuat Penempatan di Modul 2, Kubernetes membuat Pod untuk menghosting contoh aplikasi Anda. Pod adalah abstraksi Kubernet yang mewakili sekelompok satu atau beberapa wadah aplikasi (seperti Docker atau rkt), dan beberapa sumber daya bersama untuk wadah tersebut. Sumber daya tersebut meliputi:

Penyimpanan bersama, sebagai Volume
Jaringan, sebagai alamat IP cluster yang unik
Informasi tentang cara menjalankan setiap wadah, seperti versi gambar wadah atau port tertentu untuk digunakan
Pod memodelkan "host logis" khusus aplikasi dan dapat berisi berbagai wadah aplikasi yang tergabung erat. Misalnya, Pod mungkin menyertakan wadah dengan aplikasi Node.js Anda dan juga wadah lain yang memberi makan data yang akan diterbitkan oleh server web Node.js. Wadah di Pod berbagi Alamat IP dan ruang port, selalu ditempatkan bersama dan dijadwalkan bersama, dan dijalankan dalam konteks bersama di Node yang sama.

Pod adalah unit atom pada platform Kubernetes. Saat kami membuat Penempatan di Kubernetes, Penempatan itu membuat Pod dengan wadah di dalamnya (sebagai lawan membuat kontainer secara langsung). Setiap Pod terikat ke Node di mana ia dijadwalkan, dan tetap di sana sampai penghentian (sesuai dengan kebijakan restart) atau penghapusan. Dalam kasus kegagalan Node, Pod identik dijadwalkan pada Node lain yang tersedia di cluster.

Ringkasan:
Polong
Nodes
Kubectl perintah utama
Pod adalah sekelompok satu atau beberapa wadah aplikasi (seperti Docker atau rkt) dan termasuk penyimpanan bersama (volume), alamat IP, dan informasi tentang cara menjalankannya.

Nodes
Pod selalu berjalan di Node. Node adalah mesin pekerja di Kubernetes dan dapat berupa mesin virtual atau fisik, tergantung pada cluster. Setiap Node dikelola oleh Master. Node dapat memiliki beberapa pod, dan master Kubernetes secara otomatis menangani penjadwalan pod melintasi Node di cluster. Penjadwalan otomatis Master memperhitungkan sumber daya yang tersedia di setiap Node.

Setiap Kubernetes Node berjalan setidaknya:

Kubelet, sebuah proses yang bertanggung jawab untuk komunikasi antara Master Kubernetes dan Node; itu mengelola Pods dan wadah berjalan di mesin.
Sebuah runtime kontainer (seperti Docker, rkt) yang bertanggung jawab untuk menarik gambar kontainer dari registri, membongkar kontainer, dan menjalankan aplikasi.
Wadah hanya boleh dijadwalkan bersama dalam satu Pod jika dipasangkan dengan erat dan perlu berbagi sumber daya seperti disk.

Troubleshooting with kubectl
Dalam Modul 2, Anda menggunakan antarmuka baris perintah Kubectl. Anda akan terus menggunakannya di Modul 3 untuk mendapatkan informasi tentang aplikasi yang digunakan dan lingkungannya. Operasi paling umum dapat dilakukan dengan perintah kubectl berikut:

kubectl get - list resources
kubectl menggambarkan - tampilkan informasi terperinci tentang suatu sumber daya
kubectl logs - mencetak log dari wadah di pod
kubectl exec - jalankan perintah pada sebuah wadah di sebuah pod
Anda dapat menggunakan perintah ini untuk melihat kapan aplikasi dikerahkan, apa status saat ini, di mana mereka berjalan dan apa konfigurasi mereka.