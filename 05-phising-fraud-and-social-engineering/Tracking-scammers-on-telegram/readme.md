# Pengalaman menelusuri pelaku penipuan via Telegram

<p align="center">
  <img src="assets/img/tele.jpeg">
</p>

Pada beberapa tahun terakhir tingkat penipuan dalam sektor keuangan online naik secara drastis, sehingga pada November 2024 pemerintah melalui otoritas jasa keuangan (OJK) membentuk tim khusus dengan nama Indonesia Anti Scam Center (IASC) untuk menerima laporan dari masyarakat dan menangani kasus penipuan yang semakin gencar. Namun, hingga saat ini sebagian besar pelapor merasa tidak puas dengan pelayanan dari tim IASC karena merasa respon yang sangat lambat dan bahkan terkesan seperti tidak dipedulikan. Setelah saya mencari tahu dari berbagai sumber ternyata jumlah pelapor per bulan oktober 2025 sudah mencapai 300 ribu laporan dengan total kerugian mencapai 7 triliun rupiah, angka yang sangat besar sekali dan ini sekaligus menjawab pertanyaan saya mengapa respon IASC sangat lambat dan bahkan terkesan laporan seperti tidak diurus, bayangkan tim khusus dengan personel yang terbatas harus menangani laporan sebanyak ini. 

Sekitar pertengahan bulan Agustus 2025 lalu saat saya sedang berselancar di media sosial, saya tertarik dengan cerita seorang korban penipuan dengan kerugian mencapai sekitar 25 juta rupiah, nilai yang cukup besar. Dengan rasa penasaran tinggi saya menghubungi korban secara pribadi dan memintanya untuk menceritakan lebih detail lagi terkait kronologi lengkapnya. Singkat cerita korban terkena penipuan saat berniat membeli sebuah laptop yang akan digunakan untuk membuat skripsi. Korban tertarik membeli sebuah laptop Asus ROG melalui aplikasi telegram dan diminta untuk mendaftar di sebuah website. Dengan keyakinan korban mengikuti arahan dari pelaku dan mentransfer uang dengan nominal 25 juta rupiah, Namun setelah beberapa waktu korban mengatakan pernah melapor ke pihak Bank namun nihil karena menurut pihak bank transaksi tersebut tercatat sebagai transaksi yang sah, lalu korban juga sempat datang ke kantor polisi setempat namun nihil juga, terakhir korban melapor ke pihak IASC namun sampai saat ini tidak ada respon balik terkait laporannya.

![gambar rog](assets/img/rog.png)

Setelah mendapat informasi yang cukup saya mulai melakukan penelusuran dan investigasi mandiri. Saya menggunakan cara-cara manual tanpa tools tertentu dengan dorking, history dns, korelasi informasi dari korban, dan deduksi pribadi. Saya juga menggunakan berbagai informasi dari sumber terbuka atau lebih dikenal dengan teknik Open source intelligence (OSINT), Dengan teknik ini juga saya berhasil mendapatkan banyak sekali informasi terkait jaringan penipuan ini.

Puncaknya pada saat saya mencoba melihat traffic pada website yang dituturkan korban, saya mendapat traffic mencurigakan dari website utama ke sebuah halaman website lain yang sepertinya digunakan sebagai control panel. Dengan sangat bersemangat dan rasa penasaran yang tinggi, saya mencoba masuk dengan menebak-nebak password berdasarkan informasi yang saya dapatkan dan setelah beberapa lama BOOM!!! akhirnya saya berhasil masuk ke sebuah halaman admin dan menemukan banyak sekali bukti yang sangat mencengangkan.

Awalnya saya kira ini hanya sebuah penipuan biasa yang dilakukan orang lokal atau pelaku amatir. Namun setelah masuk dan melihat laman ini, saya menjadi sangat yakin bahwa ini merupakan sindikat internasional yang terstruktur dengan pusat operasi dari sebuah negara di Asia (Saya tidak akan menyebut lokasi detail). Dari informasi dan bukti yang saya dapatkan pelaku menggunakan skema fonzi dengan korban berjumlah ratusan hingga ribuan orang dengan total kerugian ratusan juta hingga mungkin Milyaran rupiah. Bahkan itu hanyalah hitungan korban yang saya dapatkan dari satu website yang mana hanya tertuju pada orang Indonesia, setelah saya telusuri lebih lanjut, ternyata sindikat ini melakukan aksinya di beberapa negara dengan jumlah korban yang tak juga sedikit. Bisa dibayangkan kerugian total dari seluruh korban dan keuntungan yang didapat pelaku.

Beberapa informasi dan bukti yang saya kumpulkan:
 
1. Rekening joki yang digunakan pelaku (saya berhasil mencatat hingga 14 rekening yang digunakan)
2. Nomor ponsel dan rekening korban
3. Beberapa alamat IP pada riwayat login yang semuanya berasal dari sebuah negara di Asia
4. Screenshoot bukti pembayaran korban dan masih banyak lagi bukti lain.

Dengan mendapatkan banyak nomor korban saya menghubungi beberapa diantarnya dan mencoba menggali informasi lebih lanjut. Ternyata pelaku menggunakan berbagai macam modus, yang terakhir pelaku menggunakan modus giveaway atau hadiah yang diberikan pada korban random melalui telegram dengan mengatasnamakan sebuah perusahaan yang ternyata setelah saya cari tahu sudah tidak beroperasi di Indonesia sejak 2020.

Terakhir, yang membuat saya sedih adalah beberapa korban yang saya hubungi mengaku sangat putus asa dan bingung harus melakukan apa dengan rata rata kerugian per orang mulai dari 10-25 juta rupiah. Beberapa rela menggadai surat berharga hingga kendaraan, Bahkan ada salah satu korban yang mengaku hampir ingin mengakhiri hidupnya karena uang yang hilang merupakan pinjaman atau hutang.

## Kesimpulan & Beberapa Langkah Menghindari Penipuan Online

Dari sini saya mendapat banyak sekali pandangan dan perspektif baru terkait kasus penipuan online yang sangat marak sekarang. Masyarakat seringkali mengeluh mengapa pemerintah dan aparat sangat lambat sekali dalam menangani kasus seperti ini, dan sekarang saya mendapat jawaban dari pengalaman ini. Setelah saya berpikir, mengapa kita harus terus menyalahkan pemerintah dan aparat yang terkesan lambat dalam hal ini ?, sementara penipuan ini terjadi karena ketidak hati-hatian dan kurangnya kita memahami dunia digital. Pada dasarnya pelaku penipuan selalu menggunakan segala cara untuk mempengaruhi korbannya. Pengetahuan dasar terkait digital awareness dan penipuan online ini menjadi sangat penting di era digital ini. Berikut beberapa hal yang harus kita pahami agar terhindar dari penipuan online:

1. Waspadai Tanda-tanda Umum Penipuan
Penipu sering kali menggunakan taktik psikologis untuk menekan korban. Waspadai hal-hal berikut: 

- Tekanan Waktu dan Ancaman: Penipu sering menciptakan rasa urgensi ("rekening Kita akan diblokir dalam 2 jam", "tawaran ini hanya berlaku 10 menit lagi"). Ini bertujuan agar Kita panik dan tidak berpikir jernih.
- Permintaan Informasi Pribadi yang Sensitif: Organisasi resmi, seperti bank atau lembaga pemerintah, tidak akan pernah meminta kata sandi lengkap, PIN, atau informasi pribadi Kita melalui email, SMS, atau telepon yang tidak diminta.
- Hadiah atau Keuntungan yang Terlalu Menggiurkan: Jika suatu penawaran terdengar terlalu bagus untuk menjadi kenyataan (misalnya, memenangkan lotre yang tidak Kita ikuti, warisan dari kerabat jauh), kemungkinan besar itu adalah penipuan.
- Permintaan Pembayaran Aneh: Penipu sering meminta pembayaran melalui metode yang sulit dilacak, seperti transfer kawat, kartu hadiah, atau mata uang kripto. 

2. Periksa Sumber Informasi (Verifikasi)
Jangan langsung memercayai email, pesan teks, atau panggilan telepon. Lakukan verifikasi secara mandiri: 

- Periksa Alamat Email dan Domain: Penipu sering menggunakan domain yang mirip dengan domain asli (misalnya, bri.co.id versus brii.co.id). Selalu periksa ejaan dengan teliti.
- Jangan Gunakan Tautan atau Nomor Telepon dari Pesan: Jika Kita menerima pesan dari bank Kita, jangan klik tautan di dalamnya atau menelepon nomor yang tertera di pesan. Sebaliknya, navigasikan langsung ke situs web resmi bank atau cari nomor layanan pelanggan mereka dari sumber tepercaya lainnya (misalnya, bagian belakang kartu kredit Kita). 

3. Jaga Keamanan Akun dan Perangkat Kita
Tindakan preventif pada perangkat Kita juga sangat penting:

- Gunakan Kata Sandi yang Kuat dan Unik: Gunakan kombinasi huruf besar, kecil, angka, dan simbol. Hindari penggunaan kata sandi yang sama untuk beberapa akun. Pertimbangkan menggunakan pengelola kata sandi.
- Aktifkan Otentikasi Dua Faktor (2FA): Ini menambahkan lapisan keamanan ekstra. Meskipun penipu mengetahui kata sandi Kita, mereka masih memerlukan kode kedua yang dikirim ke ponsel atau email Kita.
- Perbarui Perangkat Lunak Secara Teratur: Perbarui sistem operasi, peramban web, dan aplikasi antivirus Kita. Pembaruan sering kali menambal celah keamanan yang dapat dieksploitasi oleh penipu.
- Hati-hati dengan Jaringan Wi-Fi Publik: Hindari melakukan transaksi perbankan atau memasukkan informasi sensitif saat terhubung ke Wi-Fi publik yang tidak aman. 

4. Edukasi Diri Sendiri

- Pahami Modus Penipuan Umum: Penipuan seringkali berulang dengan pola yang sama, seperti penipuan dengan skema fonzi, penipuan dukungan teknis, atau penipuan investasi palsu. Semakin kita tahu tentang cara kerjanya, semakin mudah kita mengenalinya.
- Jika Ragu, Abaikan Saja: Lebih baik kehilangan penawaran yang sah daripada kehilangan uang kita karena penipuan. Jika Kita merasa tidak yakin atau tidak nyaman, mundur dan cari pendapat kedua.

Dengan memahami dasar-dasar ini, kita dapat membangun pertahanan yang kuat terhadap sebagian besar upaya penipuan online.
