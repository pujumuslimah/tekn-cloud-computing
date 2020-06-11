Pengguna mengharapkan aplikasi tersedia setiap saat dan pengembang diharapkan untuk menyebarkan versi baru beberapa kali sehari. Di Kubernetes ini dilakukan dengan menggulirkan pembaruan. Pembaruan bergulir memungkinkan pembaruan Penyebaran berlangsung tanpa henti dengan secara bertahap memperbarui mesin Pods dengan yang baru. Pod baru akan dijadwalkan di Nodes dengan sumber daya yang tersedia.

Dalam modul sebelumnya kami meningkatkan aplikasi kami untuk menjalankan beberapa instance. Ini adalah persyaratan untuk melakukan pembaruan tanpa mempengaruhi ketersediaan aplikasi. Secara default, jumlah maksimum Pods yang tidak dapat tersedia selama pembaruan dan jumlah maksimum Pods baru yang dapat dibuat, adalah satu. Kedua opsi dapat dikonfigurasikan ke angka atau persentase (dari Pod). Di Kubernetes, pembaruan diversi versi dan pembaruan Deployment apa pun dapat dikembalikan ke versi (stabil) sebelumnya.

Ringkasan:
Memperbarui aplikasi
Pembaruan bergulir memungkinkan pembaruan Penyebaran berlangsung tanpa henti dengan secara bertahap memperbarui mesin Pods dengan yang baru.

Mirip dengan Penskalaan aplikasi, jika Penyebaran diekspos secara publik, Layanan akan menyeimbangkan lalu lintas hanya ke Pod yang tersedia selama pembaruan. Pod yang tersedia adalah instance yang tersedia untuk pengguna aplikasi.

Pembaruan bergulir memungkinkan tindakan berikut:

Promosikan aplikasi dari satu lingkungan ke lingkungan lain (melalui pembaruan gambar wadah)
Kembalikan ke versi sebelumnya
Integrasi berkelanjutan dan Pengiriman aplikasi Berkesinambungan dengan downtime nol