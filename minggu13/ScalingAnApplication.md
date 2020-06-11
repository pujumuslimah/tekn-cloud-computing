Menurunkan Penyebaran akan memastikan Pod baru dibuat dan dijadwalkan ke Node dengan sumber daya yang tersedia. Penskalaan akan meningkatkan jumlah Pod ke keadaan yang diinginkan baru. Kubernetes juga mendukung autoscaling Pods, tetapi di luar cakupan tutorial ini. Penskalaan ke nol juga dimungkinkan, dan itu akan menghentikan semua Pod dari Penempatan yang ditentukan.

Menjalankan banyak contoh aplikasi akan membutuhkan cara untuk mendistribusikan lalu lintas ke semuanya. Layanan memiliki penyeimbang beban terintegrasi yang akan mendistribusikan lalu lintas jaringan ke semua Pods dari Penempatan yang terbuka. Layanan akan memantau secara terus-menerus Pod yang sedang berjalan menggunakan titik akhir, untuk memastikan lalu lintas dikirim hanya ke Pod yang tersedia.

