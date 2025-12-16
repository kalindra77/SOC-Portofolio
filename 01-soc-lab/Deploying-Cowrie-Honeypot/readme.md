# Deploying Cowrie (Honeypot)

<p align='center'>
  <img src='assets/img/honeypot.jpg' width='400'>
</p>

Salah satu metode yang digunakan untuk mengecoh dan menganalisis perilaku penyerang adalah menerapkan honeypot pada sistem. Cowrie merupakan open-source honeypot berbasis SSH dan Telnet yang dirancang untuk mengecoh, menangkap, dan merekam aktivitas penyerang dalam sistem. Seluruh aktivitas yang dilakukan oleh penyerang, seperti percobaan login, perintah yang dijalankan, hingga file yang diunduh, akan direkam untuk keperluan analisis. Dengan demikian, penggunaan honeypot Cowrie dapat menjadi alat yang efektif dalam mempelajari ancaman keamanan jaringan serta meningkatkan strategi pertahanan sistem di masa mendatang.

## Deploy cowrie dengan docker

Disini saya akan menerapkan cowrie menggunakan docker. Dengan docker kita hanya perlu mengunduh image yang sudah dibuat lalu menjalankan cowrie pada sistem lokal. Saya akan mencoba konfigurasi ssh agar semua traffic selain dari interface VPN yang sudah ditentukan akan dialihkan menuju cowrie tanpa memindahkan port default SSH itu sendiri dengan menggunakan IPtables.

- Pull image cowrie dari docker hub

```bash
sudo docker pull cowrie/cowrie:latest
```
- Jika telah selesai cek apakah image cowrie telah ada di docker lokal

```bash
sudo docker images
```
![docker images](assets/img/docker-images.png)

- Jika ada lanjut jalankan cowrie dengan docker, disini kita tidak akan mempublish port docker ke interface host, karena tujuannya mengecoh penyerang maka kita akan tetap menggunakan port 22 SSH namun selain koneksi yang masuk dari interface wg0 (wireguard VPN) maka akan dialihkan ke honeypot.

```bash
sudo docker run -d --name cowrie -p 172.17.0.1:2222:2222 --restart unless-stopped cowrie/cowrie

penjelasan:

-d        : jalankan docker sebagai di background 
--name    : beri nama container cowrie
-p        : 172.17.0.1 adalah interface virtual (docker0) yang dibuat oleh docker bisa dicek dengan perintah ip a. 2222:2222 publis port 2222 container ke port 2222 interface docker0
--restart : unless-stopped jalankan otomatis container setelah docker reboot 
```
- Untuk memastikan container sudah jalan dengan benar cek dengan perintah

```bash
sudo docker ps
```
![docker-ps](assets/img/docker-ps.png)

- Setelah coba akses ssh cowrie untuk memastikan sudah berjalan dengan benar. untuk usernya root dan password bisa diisikan bebas

```bash
ssh -p 2222 root@172.17.0.1
```
- jika berhasil login maka container cowrie sudah berjalan dengan benar. Sekarang tinggal konfigurasi iptables agar setiap akses diluar VPN dialihkan ke honeypot 
