# Rhino Scenario

Disini saya menggunakan skenario rhino yang mana kita diberi tugas menganalisa dan mencari jejak pada file hasil dump yang telah diberikan untuk mengungkap sebuah kasus 

Saya akan coba menganalisa, mengidentifikasi, dan mencari bukti-bukti pada file RHINOUSB.dd dan traffic jaringan yang sudah ditangkap dalam bentuk bebrapa file log.

Saya Menggunakan tools yaitu autopsy dan the sleuth kit untuk menganalisa file dump usb juga Wireshark dan Bruteforcesharkcli untuk file log jaringannya

## Yang pertama analisa dump usb menggunakan The sleuth kit

![Gambar fsstat](assets/img/fsstat.png)
- Gunakan perintah fsstat untuk melihat filesystem status detail, disini file menggunakan format FAT-16

