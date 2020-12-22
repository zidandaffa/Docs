# 3 Tahap Membuka Password Windows dengan Ubuntu
Sumber: http://www.detikinet.com/read/2010/10/13/141552/1463843/510/3-tahap-membuka-password-windows-dengan-ubuntu?hlight

Lupa memang masalah yang biasa dihadapi manusia. Jika lupa password login Windows, ada cara untuk memulihkannya dengan menggunakan sistem operasi Ubuntu Linux.

## Langkah 1
Hal pertama yang perlu dilakukan adalah membuat Live CD atau Live USB Flashdisk Ubuntu Linux. Ubuntu Live ini akan digunakan untuk booting ke sistem dan melakukan prosedur yang dibutuhkan untuk membongkar password Windows tadi.

Cara paling mudah untuk melakukan itu adalah dengan men-download UNetBootin dan menjalankannya. Aplikasi sederhana ini akan men-download versi Ubuntu yang dipilih dan melakukan instalasi pada flashdisk yang Anda siapkan.

## Langkah 2
Tahap kedua adalah menginstall utility Open Source bernama chntpw. Hal ini dilakukan dari Ubuntu dengan menjalankan Synaptic Package Manager.

Untuk bisa mendapatkan chntpw, Synaptic Package Manager harus diarahkan untuk melihat pada penyimpanan aplikasi Universe. Hal itu bisa dilakukan dengan mengklik menu Settings > Repositories pada jendela Synaptic. Kemudian, centang pilihan 'Community-maintained Open Source software (universe)' dan klik Close.

Setelah itu, klik tombol Reload dan Synaptic akan men-download informasi paket terbaru dari Universe. Setelah selesai, ketikkan chntpw pada kotak Quick Search.

Jika sudah muncul, centang kotak di sisi tulisan chnptw, pilih 'Mark for Installation'. Lalu klik Apply untuk menginstalnya.

Atau menggunakan cara

```
apt-get install chnptw 
```
Pastikan chnptw menggunakan perintah

```
apt-cache search chnptw
```
Untuk komputer 64bit, gunakan cara
```
https://packages.debian.org/sid/amd64/chntpw/download
```
Edit /etc/apt/sources.list
```
deb http://ftp.de.debian.org/debian sid main 
```
Lakukan
```
apt-get update
apt-get install chnptw
```
## Langkah 3
Tahap ketiga adalah mengubah password Windows dengan chntpw.

Mount hardisk / drive yang berisi instalasi Windows Anda
Buka hardisk itu (klik Places) dan catat label drive yang muncul pada menu bar jendela file browser
Buka jendela Terminal (Applications > Accessories > Terminal)
Ketik perintah berikut pada Terminal:
```
cd / media
ls
```
Ketik: cd [label hardisk yang tadi Anda catat]
ketik: cd WINDOWS/system32/config
Untuk mengubah password Administrator, ketikkan perintah: sudo chntpw SAM
kan muncul beberapa perintah yang bisa Anda pilih, perintah paling aman adalah membuat password jadi kosong. Lakukan ini dengan menekan angka '1', lalu tekan 'y' untuk konfirmasi
Pilih '2' untuk mengubah password ke kata tertentu, namun hal ini memiliki risiko error lebih besar
Untuk mengubah password user lain (non-administrator), ketikkan perintah berikut (dari Terminal):
```
sudo chntpw –u [nama user] SAM
```

## Referensi
* http://www.detikinet.com/read/2010/10/13/141552/1463843/510/3-tahap-membuka-password-windows-dengan-ubuntu?hlight
* http://dailytechnologiesupdate.blogspot.com/2011/03/reset-windows-7-password-with-ubuntu.html