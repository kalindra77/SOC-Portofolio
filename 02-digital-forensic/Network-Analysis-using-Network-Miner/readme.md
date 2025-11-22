# Network Analysis Using Network Miner

<p align="center">
<img src="assets/img/networkminer.png" width="400">
</p>

Network Miner merupakan Network forensics tools yang biasa digunakan dalam digital forensik untuk mengekstraksi dan memetakan traffic network. Network miner banyak diminati karena sederhana dan mudah digunakan. Network-miner memberikan mapping traffic jaringan yang mudah dipahami dan user friendly. Berbeda dengan wireshark yang mana kita harus membuat mapping mandiri namun lebih powerfull dalam hasil analisis, sehingga network-miner menurut saya hanya cocok untuk analisa tahap awal atau analisa cepat. Network Miner dapat di unduh melali situs resmi https://www.netresec.com/?page=NetworkMiner 

## Analisis Menggunakan Network Miner 

Dalam digital forensik traffic network merupakan salah satu sumber data yang sangat kaya. Karena Network dapat menyimpan berbagai lalu lintas jaringan yang digunakan oleh user atau threat actor. Contoh credential dalam plain text seperti ftp yang dapat dengan mudah ditemukan dalam traffic network, data stream yang dapat dipulihkan menjadi file utuh, rekaman VoIP yang lewat, dan masih banyak lagi. Oleh karena itu menganalisa network traffic menjadi salah satu bagian penting dalam digital forensik.

- Pertama kita harus menangkap traffic jairngan untuk dianalisa atau kita bisa menggunakan sample traffic yang didapat dari internet.

[gambar network dump](assets/img/network-dump.png)

- Setelah itu kita dapat membuka file pcap yang sudah ditangkap dari dalam network-miner dan ini hasil yang ditampilkan network-miner

[gambar network miner](assets/img/dashboard-nm.png)

- Fitur yang diberikan network-miner dalam versi gratis cukup terbatas, oleh karena itu kita hanya dapat menjelajahi fitur fitur dasar yang tersedia seperti yang dapat dilihat pada navigation bar diatas.

## Kesimpulan

Ketika saya menggunakan network-miner saya menyimpulkan bahwa tools ini hanya cocok untuk analisa tahap awal dan analisa cepat bukan deep anlysis. Terlebih dalam versi gratis beberapa fitur dibatasi sehingga cukup menyulitkan dalam proses dan insiden yang butuh deep analysis. Oleh karena itu tools open-source seperti wireshark mungkin lebih relevan pada beberapa kasus yang butuh anlisis lebih dalam dan yang butuh fleksibiitas tinggi.   


