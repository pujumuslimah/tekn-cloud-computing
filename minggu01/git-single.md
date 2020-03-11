LATIHAN

1.	INSTAL GIT DI WINDOWS
a.	Setelah download Git, double click pada file yang di-download. Akan dimunculkan lisensi. Klik Next untuk lanjut.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar1.jpg

b.	Pilih komponen. Tidak perlu diubah-ubah, sesuai dengan default saja. Klik pada Next.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar2.jpg

c.	Pilih editor yang akan digunakan bersama dengan Git. Pada pilihan ini, digunakan Notepad++.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar3.jpg

d.	Pada saat instalasi, Git menyediakan akses git melalui Bash maupun command prompt. Pilih pilihan kedua supaya bisa menggunakan dari dua antarmuka tersebut. Bash adalah shell di Linux. Dengan menggunakan bash di Windows, pekerjaan di command line Windows bisa dilakukan menggunakan bash - termasuk ekskusi dari Git.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar4.jpg

e.	Pilih OpenSSL untuk HTTPS. Git menggunakan https untuk akes ke repo GitHub atau repo-repo lain (GitLab, Assembla).

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar5.jpg

f.	Pilih pilihan pertama untuk konversi akhir baris (CR-LF).

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar6.jpg

g.	Pilih PuTTY untuk terminal yang digunakan untuk mengakses Git Bash.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar7.jpg

h.	Untuk opsi ekstra, pilih serta aktifkan 1 dan 2.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar8.jpg

i.	 Setelah itu proses instalasi akan dilakukan.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar9.jpg

j.	Jika selesai akan muncul dialog pemberitahuan. Klik pada Finish.

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar10.jpg

k.	Untuk menjalankan, dari Start menu, ketikkan "Git", akan muncul beberapa pilihan. Pilih "Git Bash" atau "Git GUI".

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar11.jpg

l.   Tampilan jika akan menggunakan "Git Bash"

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar12.jpg

m. Tampilan jika akan menggunakan "Git GUI"

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar13.jpg

n.	Untuk mencoba dari command prompt, masuk ke command prompt, setelah itu eksekusi "git --version" untuk melihat apakah sudah terinstall atau belum. Jika sudah terinstall dengan benar, makan akan muncul hasil berikut:

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar14.jpg


2.	KONFIGURASI GIT
a.	Konfigurasi username dan email

puji@DESKTOP-6CBNPJM MINGW64 ~
$ cd C:/minggu01

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01
$ git config --global user.name "pujumuslimah"

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01
$ git config --global user.email pujimuslimah2007@gmail.com


b.	melihat konfigurasi yang sudah ada

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01
$ git config --list
core.symlinks=false
core.autocrlf=true
core.fscache=true
color.diff=auto
color.status=auto
color.branch=auto
color.interactive=true
help.format=html
http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
diff.astextplain.textconv=astextplain
rebase.autosquash=true
credential.helper=manager
user.name=pujumuslimah
user.email=pujimuslimah2007@gmail.com



3.	MENGELOLA REPO SENDIRI

A.	Mengelola repo sendiri di account sendiri

1. Klik tanda + pada bagian atas setelah login, pilih New repository

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar15.jpg

2. Isikan nama, keterangan, serta lisensi. Jika dikehendaki, bisa membuat repo Private

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar16.jpg

3. Klik Create Repository

4. melakukan proses clone repo

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01
$ git clone https://github.com/pujumuslimah/tekn-cloud-computing
Cloning into 'tekn-cloud-computing'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.

5. Mengubah Isi - Push Tanpa Branching dan Merging
Perubahan isi bisa terjadi karena satu atau kombinasi beberapa hal berikut:
a. File dihapus
b. File diedit
c. Membuat file / direktori baru
d. Menghapus direktori
Untuk kasus-kasus tersebut, lakukan perubahan di komputer lokal, setelah itu push ke repo :

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01
$ cd tekn-cloud-computing/
puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git add -A
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory.

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git commit -m "Add: README.md"
[master 668dd19] Add: README.md
 1 file changed, 1 insertion(+), 1 deletion(-)

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git push origin master
Fatal: HttpRequestException encountered.
   An error occurred while sending the request.
Username for 'https://github.com': pujumuslimah
Counting objects: 3, done.
Writing objects: 100% (3/3), 275 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/pujumuslimah/tekn-cloud-computing
   783f1ba..668dd19  master -> master

6. Mengubah Isi dengan Branching and Merging
cara untuk "membersihkan" repo lokal :
- Buat branch untuk menampung perubahan-perubahan
- Lakukan perubahan-perubahan
- Add dan commit perubahan-perubahan tersebut ke branch
- Kembali ke repo master
- Buat pull request di GitHub
- Merge pull request di GitHub
- Merge branch untuk menampung perubahan-perubahan tersebut ke master.
- Selesai.

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git checkout -b edit-readme-1
Switched to a new branch 'edit-readme-1'
puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (edit-readme-1)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (edit-readme-1)
$ cat README.md
# tekn-cloud-computing


ini isi proyek

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (edit-readme-1)
$ git status
On branch edit-readme-1
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (edit-readme-1)
$ git add -A
warning: LF will be replaced by CRLF in README.md.
The file will have its original line endings in your working directory.

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (edit-readme-1)
$ git commit -m "Add: isi README.md"
[edit-readme-1 6cb4215] Add: isi README.md
 1 file changed, 3 insertions(+)

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (edit-readme-1)
$ git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git push origin edit-readme-1
Fatal: HttpRequestException encountered.
   An error occurred while sending the request.
Username for 'https://github.com': pujumuslimah
Counting objects: 3, done.
Writing objects: 100% (3/3), 294 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'edit-readme-1' on GitHub by visiting:
remote:      https://github.com/pujumuslimah/tekn-cloud-computing/pull/new/edit-readme-1
remote:
To https://github.com/pujumuslimah/tekn-cloud-computing
 * [new branch]      edit-readme-1 -> edit-readme-1


7. kirim pul ke riquest PR

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar17.JPG
https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar18.JPG

8. Confirm Merge, branch yang kita kirimkan tadi sudah dimasukkan ke branch master. Setelah itu, merge di komputer lokal:

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git merge edit-readme-1
Updating 668dd19..6cb4215
Fast-forward
 README.md | 3 +++
 1 file changed, 3 insertions(+)

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git branch -D edit-readme-1
Deleted branch edit-readme-1 (was 6cb4215).

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git branch
* master

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git pull
Already up-to-date.

9. Perintah untuk sinkronisasi adalah:
$ git pull

10. Membatalkan Perubahan

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git checkout -b edit-readme-2
Switched to a new branch 'edit-readme-2'

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (edit-readme-2)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (edit-readme-2)
$ cat README.md
# tekn-cloud-computing


ini isi proyek. jadi agak kacau nih

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (edit-readme-2)
$ git checkout master
M       README.md
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing


ini isi proyek. jadi agak kacau nih

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git branch -D edit-readme-2
Deleted branch edit-readme-2 (was 668dd19).

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git branch
* master

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing


ini isi proyek. jadi agak kacau nih

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git reset --hard
HEAD is now at 668dd19 Add: README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing


11. Undo Commit Terakhir

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

ini isi proyek

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git log --oneline
668dd19 Add: README.md
783f1ba Initial commit

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git add -A

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git commit -m "Add: contents"
[master 70b3723] Add: contents
 1 file changed, 2 insertions(+)

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git push origin master
Fatal: HttpRequestException encountered.
   An error occurred while sending the request.
Username for 'https://github.com': pujumuslimah
Counting objects: 3, done.
Writing objects: 100% (3/3), 285 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/pujumuslimah/tekn-cloud-computing
   668dd19..70b3723  master -> master

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git add -A

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git commit -m "add: contents -2"
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git commit -m "Add: contents -2"
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git push origin master
Fatal: HttpRequestException encountered.
   An error occurred while sending the request.
Username for 'https://github.com': pujumuslimah
Everything up-to-date

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git commit -m "Add: contents - 2"
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

ini isi proyek

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

ini isi proyek

ini isi 1

ini isi 2

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git revert HEAD
error: Your local changes to the following files would be overwritten by merge:
        README.md
Please commit your changes or stash them before you merge.
Aborting
fatal: revert failed

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git push origin master
Fatal: HttpRequestException encountered.
   An error occurred while sending the request.
Username for 'https://github.com': pujumuslimah
Everything up-to-date

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

ini isi proyek

ini isi 1

ini isi 2

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

ini isi proyek

ini isi 1

ini isi tambahan 1

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git add -A

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git commit -m "Add: isi tambahan 1"
[master 9fe5336] Add: isi tambahan 1
 1 file changed, 4 insertions(+)

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
nothing to commit, working tree clean

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git log --oneline
9fe5336 Add: isi tambahan 1
70b3723 Add: contents
668dd19 Add: README.md
783f1ba Initial commit

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git reset --hard HEAD^
HEAD is now at 70b3723 Add: contents

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

ini isi proyek

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

ini isi proyek

ini isi 1

ini isi 2

ini isi 3

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git log --oneline
70b3723 Add: contents
668dd19 Add: README.md
783f1ba Initial commit

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git rerevert 70b3723
git: 'rerevert' is not a git command. See 'git --help'.

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

ini isi proyeks

ini isi 1

<<<<<<< HEAD
ini isi 2

ini isi 3
=======
>>>>>>> parent of 70b3937... ADD: isi 1

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ vim README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ cat README.md
# tekn-cloud-computing

ini isi proyek

ini isi 1

ini isi 2 setelah revert

ini isi 3

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git add README.md

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   README.md


puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git revert --continue
error: no cherry-pick or revert in progress
fatal: revert failed

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   README.md


puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git revert --continue
error: no cherry-pick or revert in progress
fatal: revert failed

puji@DESKTOP-6CBNPJM MINGW64 /c/minggu01/tekn-cloud-computing (master)
$ git push origin master
Fatal: HttpRequestException encountered.
   An error occurred while sending the request.
Username for 'https://github.com': pujumuslimah
Everything up-to-date


B.	Mengelola Repo Sendiri di Organisasi

https://github.com/pujumuslimah/tekn-cloud-computing/blob/master/minggu01/gambar19.JPG
