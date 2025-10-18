# Rhino Scenario

Disini saya menggunakan skenario rhino yang mana kita diberi tugas menganalisa dan mencari jejak pada file hasil dump yang telah diberikan untuk mengungkap sebuah kasus 

Tugasnya adalah memulihkan setidaknya sembilan gambar badak dari bukti yang tersedia dan memasukkannya ke dalam laporan singkat

• Siapa yang memberi terdakwa akun telnet/ftp?

• Apa nama pengguna/kata sandi untuk akun tersebut?

• Transfer berkas relevan apa yang muncul dalam jejak jaringan?

• Apa yang terjadi pada hard drive di komputer? Di mana sekarang?

• Apa yang terjadi pada key USB?

• Apa yang dapat dipulihkan dari image dd USB?

Apakah ada bukti yang menghubungkan kunci USB dan jejak jaringan? Jika ada, apa?

Saya akan coba menganalisa, mengidentifikasi, dan mencari bukti-bukti pada file RHINOUSB.dd dan traffic jaringan yang sudah ditangkap dalam bentuk bebrapa file log.

Saya Menggunakan tools yaitu autopsy dan the sleuth kit untuk menganalisa file dump usb juga Wireshark dan Bruteforcesharkcli untuk file log jaringannya

## Menganalisa file log network traffic menggunakan Wireshark

Selanjutnya setelah menganalisa dump usb, ternyata tidak ditemukan hal-hal yang mencurigakan, dalam file zip ini ada 3 buah log file yang berisi log traffic jaringan, untuk melanjutkan investigasi saya menggunakan wireshark untuk menganalisa log traffic ini

![Gambar filter](assets/img/filter_ftp_userpass.png)
- Buka file dengan wireshark lalu gunakan filter **ftp or ftp-data** untuk melihat lalu lintas ftp pada log, dapat dilihat di atas ada user dan password ftp yang tidak terenkripsi pertanyaan username dan password terjawab username: gnome password: gnome123

![Gambar log](assets/img/filter_ftp_send.png)
- Bisa dilihat ada traffic pengiriman data melalui ftp dengan nama file rhino1.jpg, kita bisa merocevery file tersebut dengan melihat raw data nya

![Gambar log](assets/img/filter_ftp_klik.png)
- Kita bisa melihat aliran data nya Dengan klik kanan pada log pertama pengriman lalu follow pilih TCP stream untuk melihat aliran data dan isi raw nya

![Gambar raw](assets/img/raw_mark.png)
- Di sini jika data berupa ASCII pada kolom show as ubah menjadi RAW lalu klik save as masukan nama file untuk disimpan

![Gambar rhino1](assets/img/rhino1.png)
- Hasilnya adalah file rhino1 yang berhasil di recover, gambar menunjukan seekor badak di alam liar
- Saya melakukan cara yang sama untuk merecoever semua file yang terdapat pada semua log tersebut termasuk file contrapand.zip

![Gambar contrapand](assets/img/zip_locked.png)

- Tampaknya file zip contrapand membutuhkan password untuk diekstraksi, saya akan menggunakan tools fcrackzip untuk membuka password tersebut

![Gambar fcrack](assets/img/fcrackzip.png)

- Gunakan perintah **fcrackzip -v -u -D -p /usr/share/wordlists/rockyou.tx contrapand.zip** untuk memecah password dengan wordlists rockyou
- Dan passwordnya adalah: monkey

![Gambar rhino2](assets/img/rhino2.png) 

- Hasilnya adalah gambar rhino2.jpg 
