Setelah Anda memiliki kluster Kubernetes yang berjalan, Anda dapat menggunakan aplikasi kemas Anda di atasnya. Untuk melakukannya, Anda membuat konfigurasi penyebaran Kubernetes. Deployment menginstruksikan Kubernetes cara membuat dan memperbarui instance aplikasi Anda. Setelah Anda membuat Penempatan, master Kubernet menjadwalkan instance aplikasi yang termasuk dalam Penempatan tersebut untuk dijalankan pada masing-masing Node di kluster.


Setelah instance aplikasi dibuat, Pengontrol Deployment Kubernetes terus memantau instance tersebut. Jika Node yang menjadi hosting instance turun atau dihapus, pengendali penyebaran menggantikan instance dengan instance pada Node lain di cluster. Ini menyediakan mekanisme penyembuhan sendiri untuk mengatasi kegagalan atau perawatan alat berat.


Dalam dunia pra-orkestrasi, skrip instalasi sering digunakan untuk memulai aplikasi, tetapi skrip instalasi tidak memungkinkan pemulihan dari kerusakan mesin. Dengan membuat instance aplikasi Anda dan membuatnya tetap berjalan melintasi Nodes, Kubernetes Deployments memberikan pendekatan yang berbeda secara mendasar terhadap manajemen aplikasi.


Deployment bertanggung jawab untuk membuat dan memperbarui instance aplikasi Anda.


Anda dapat membuat dan mengelola Penyebaran dengan menggunakan antarmuka baris perintah Kubernetes, Kubectl. Kubectl menggunakan API Kubernetes untuk berinteraksi dengan cluster. Dalam modul ini, Anda akan mempelajari perintah Kubectl paling umum yang diperlukan untuk membuat Penyebaran yang menjalankan aplikasi Anda di kluster Kubernetes.


Saat Anda membuat Penempatan, Anda harus menentukan gambar wadah untuk aplikasi Anda dan jumlah replika yang ingin Anda jalankan. Anda dapat mengubah informasi itu nanti dengan memperbarui Penempatan Anda; Modul 5 dan 6 dari bootcamp membahas bagaimana Anda dapat mengukur dan memperbarui Penyebaran Anda.


Aplikasi perlu dikemas ke dalam salah satu format wadah yang didukung untuk digunakan di Kubernetes


Untuk Penempatan pertama Anda, Anda akan menggunakan aplikasi Node.js yang dikemas dalam wadah Docker. (Jika Anda belum mencoba membuat aplikasi Node.js dan menggunakannya menggunakan wadah, Anda dapat melakukannya terlebih dahulu dengan mengikuti instruksi dari tutorial Hello Minikube).