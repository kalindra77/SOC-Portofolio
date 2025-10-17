# Rhino Scenario

Disini saya menggunakan skenario rhino yang mana kita diberi tugas menganalisa dan mencari jejak pada file hasil dump yang telah diberikan untuk mengungkap sebuah kasus 

Saya akan coba menganalisa, mengidentifikasi, dan mencari bukti-bukti pada file RHINOUSB.dd dan traffic jaringan yang sudah ditangkap dalam bentuk bebrapa file log.

Saya Menggunakan tools yaitu autopsy dan the sleuth kit untuk menganalisa file dump usb juga Wireshark dan Bruteforcesharkcli untuk file log jaringannya

## Yang pertama analisa dump usb menggunakan The sleuth kit

![Gambar fsstat](assets/img/fsstat.png)
- Gunakan perintah fsstat untuk melihat filesystem status secara detail, disini kita mendapat informasi seperti tipe file system yaitu FAT-16, Informasi metadata serta sector yang digunakan

![Gambar fls](assets/img/fls.png)
- Gunakan perintah fls untuk meihat isi dari dump usb, tampak ada dua file pada gambar yaitu gumbo1.txt dengan inode 4 dan gumbo2.txt dengan inode 6. Dalam beberapa kasus file di dalam dump sudah dihapus untuk melihat file yang telah dihapus dapat menggunakan flag -d pada perintah menjadi fls -d juga flag -r untuk menampilkan file secara recursive

![Gambar istat](assets/img/istat.png)
- Gunakan perintah istat ditambah inode yang sudah didapat untuk melihat status inode dari sebuah file. Disini kita dapat melihat informasi detail file tersebut mulai dari size, nama, metadata waktu dibuat, diakses dan terakhir ditulis hingga sektor mana saja yang digunakan oleh file tersebut

![Gambar icat](assets/img/icat.png)
- Terakhir gunakan perintah icat untuk menampilkan isi dari file gumbo1.txt 

