# Pengalaman menelusuri pelaku penipuan via Telegram

<p align="center">
  <img src="assets/img/tele.jpeg">
</p>

Pada beberapa tahun terakhir tingkat penipuan dalam sektor keuangan online naik secara drastis, sehingga pada November 2024 pemerintah melalui otoritas jasa keuangan (OJK) membentuk tim khusus dengan nama Indonesia Anti Scam Center (IASC) untuk menerima laporan dari masyarakat dan menangani kasus penipuan yang semakin gencar. Namun, hingga saat ini sebagian besar pelapor merasa tidak puas dengan pelayanan dari tim IASC karena merasa respon yang sangat lambat dan bahkan terkesan seperti tidak dipedulikan. Setelah saya mencari tahu dari berbagai sumber ternyata jumlah pelapor per bulan oktober 2025 sudah mencapai 300 ribu laporan dengan total kerugian mencapai 7 triliun rupiah, angka yang sangat besar sekali dan ini sekaligus menjawab pertanyaan saya mengapa respon IASC sangat lambat dan bahkan terkesan laporan seperti tidak diurus, bayangkan tim khusus dengan personel yang terbatas harus menangani laporan sebanyak ini. 

Sekitar pertengahan bulan Agustus 2025 lalu saat saya sedang berselancar di media sosial, saya tertarik dengan cerita seorang korban penipuan dengan kerugian mencapai sekitar 25 juta rupiah, nilai yang cukup besar. Dengan rasa penasaran tinggi saya menghubungi korban secara pribadi dan memintanya untuk menceritakan lebih detail lagi terkait kronologi lengkapnya. Singkat cerita korban terkena penipuan saat berniat membeli sebuah laptop yang akan digunakan untuk membuat skripsi. Korban tertarik membeli sebuah laptop Asus ROG melalui aplikasi telegram dan diminta untuk mendaftar di sebuah website. Dengan keyakinan korban mengikuti arahan dari pelaku dan mentransfer uang dengan nominal 25 juta rupiah, Namun setelah beberapa waktu korban mengatakan pernah melapor ke pihak Bank namun nihil karena menurut pihak bank transaksi tersebut tercatat sebagai transaksi yang sah, lalu korban juga sempat datang ke kantor polisi setempat namun nihil juga, terakhir korban melapor ke pihak IASC namun sampai saat ini tidak ada respon balik terkait laporannya.

![gambar rog](assets/img/rog.png)

Setelah mendapat informasi yang cukup saya mulai melakukan penelusuran dan investigasi mandiri. Saya menggunakan cara-cara manual tanpa tools tertentu dengan dorking, history dns, korelasi informasi dari korban, dan deduksi pribadi. Saya juga menggunakan berbagai informasi dari sumber terbuka atau lebih dikenal dengan teknik Open source intelligence (OSINT), Dengan teknik ini juga saya berhasil mendapatkan banyak sekali informasi terkait jaringan penipuan ini.

Puncaknya pada saat saya mencoba melihat traffic pada website yang dituturkan korban, saya mendapat traffic mencurigakan dari website utama ke sebuah halaman website lain yang sepertinya digunakan sebagai control panel. Dengan sangat bersemangat dan rasa penasaran yang tinggi, saya mencoba masuk dengan menebak-nebak password berdasarkan informasi yang saya dapatkan dan setelah beberapa lama BOOM!!! akhirnya saya berhasil masuk ke sebuah halaman admin dan menemukan banyak sekali bukti yang sangat mencengangkan.

Awalnya saya kira ini hanya sebuah penipuan biasa yang dilakukan orang lokal atau pelaku amatir. Namun setelah masuk dan melihat laman ini, saya menjadi sangat yakin bahwa ini merupakan sindikat internasional yang terstruktur dengan pusat operasi dari sebuah negara di Asia (Saya tidak akan menyebut lokasi detail). Dari sini saya mulai sangat bersemangat untuk menelusuri lebih lanjut.

Saya berhasil mendapat banyak sekali informasi dan bukti diantaranya:
 
1. Rekening joki yang digunakan pelaku (saya berhasil mencatat hingga 14 rekening yang digunakan)
2. Nomor ponsel dan rekening korban
3. Beberapa alamat IP pada riwayat login yang semuanya berasal dari sebuah negara di Asia
4. Screenshoot bukti pembayaran korban dan masih banyak lagi bukti lain.

Dengan mendapatkan banyak nomor korban saya menghubungi beberapa diantarnya dan mencoba menggali informasi lain. Ternyata pelaku menggunakan berbagai macam modus, yang terakhir pelaku menggunakan modus giveaway atau hadiah yang diberikan pada korban random melalui telegram dengan mengatasnamakan sebuah perusahaan yang ternyata setelah saya cari tahu sudah tidak beroperasi di Indonesia sejak 2020.
