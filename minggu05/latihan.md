INSTALL JAVA

1. install java
$ sudo apt-get install oracle-java8-installer

2. Setelah instalasi, lakukan pengecekan pada sistem Perintah ini akan mendaftar 
semua versi yang terinstal dengan tanda aktif saat ini dan menyediakan dialog untuk beralih. 

4. Ada 3 pilihan untuk alternatif java.



EDIT .bashrc file

1. Lakukan proses editing pada JAVA_HOME yang terletak pada file .bashrc.
$ vi .bashrc
$ export JAVA_HOME=/usr/lib/jvm/java-8-oracle


INSTALL APACHE OFBIz
1. Kami menggunakan apache OFBIz 16.11.03 (versi stabil) Catatan: Pilih versi stabil di menu ‘releases’. 
$ sudo apt install subversion

2. Untuk menginstal dan menyalakan apache OFBiz dengan cepat
$ ./gradlew cleanAll loadDefault
$ ./gradlew ofbiz

