# Linux System Hardening

<p align="center">
  <img src="assets/img/linux.jpeg" width="400">
</p>

Hardening sistem berarti mengunci, memperkuat, atau meminimalkan permukaan serangan sehingga dapat menghambat attacker saat menjalankan aksinya. Menghapus software yang tidak diperlukan, Mengonfigurasi default values ke pengaturan seketat mungkin, dan Menjalankan hanya apa yang kita butuhkan secara eksplisit. Contoh dalam kehidupan sehari-hari, Sebuah toko perhiasaan akan menggunakan keamanan ekstra saat sedang tutup malam hari entah dengan kunci besar dan lebih kuat atau bahkan dengan menaruh seorang security guard disana, tujuannya tak lain adalah meminimalkan resiko dan mengurangi permukan serangan yang dapat dilakukan oleh pencuri.

## Mengapa Hardening Penting ?

Siapa pun yang menjalankan infrastuktur sistem komputer apalagi mengelola dan menyimpan data penting mesti khawatir terhadap keamanan sistemnya. Sesuai dengan salah satu prinsip cybersecurity yang tidak tertulis yaitu: "No system is safe" Tidak ada sistem yang aman, bahkan sekuat-kuatnya infrastukur keamanannya attacker selalu mempunyai cara dan celah yang dapat digunakan. Dalam peraturan pemerintah setiap negara, kebocoran data atau pelanggaran privasi pelanggan baik disengaja maupun tidak memiliki hukuman atau konsekuensi tertentu seperti denda atau pencabutan izin operasi, belum lagi tercorengnya reputasi organisasi tersebut yang makin memperburuk dampaknya.

## 5 Langkah Hardening

Saya akan memberi 5 langkah dasar hardening linux, tentu ini bukan hardening lengkap karena menyesuaikan dengan perangkat yang saya gunakan namun ini merupakan langkah awal yang mungkin perlu diterapkan. **DISCLAIMER!**: Saya menggunakan distro linux ubuntu sehingga mungkin akan berbeda prosesnya dengan distro linux yang lain.

### 1. Pastikan sistem selalu up-to-date

Ini hal yang sering disepelekan namun dapat berakibat fatal jika tidak dilakukan. Pengembang selalu melakukan patch celah keamanan pada sistem dan program di linux melalui proses update. Oleh karena itu jika kita mengabaikan proses ini attacker dapat dengan mudah masuk dengan melakukan eksploitasi pada celah yang belum ditambal pada sistem kita. Contoh: SMBv1 memiliki celah yang dikenal engan eternal-blue yang dimanfaatkan oleh ransomware seperti wanna-cry, oleh karena itu pada versi update selanjutnya pengembang melakukan patch pada celah tersebut dan menutup akses attacker.

### 2. Hapus program atau komponen yang tidak diperlukan

Semakin banyak program atau komponen, semakin luas juga attack vector yang muncul. Secara default biasanya distro linux yang sudah built-in atau easy-install seperti ubuntu, membawa banyak program atau tools yang tidak benar benar digunakan dan hanya menjadi bloatware. Ini dapat menurunkan kinerja perangkat dan memunculkan attack vector yang tidak kita sadari.

### 3. Konfigurasi logging

Dalam linux setiap program memiliki file logging tersendiri yang biasanya dapat ditemukan dalam direktori **/var/log/** atau sesuai dengan konfigurasi program tersebut.Fungsi logging adalah mencatat segala aktivitas user saat berada dalam linux. Ketika terjadi kompromi pada sistem, file log adalah file yang pertama kali diperiksa untuk mendapatkan Indicator of Compromise (IoC) dan mencari jejak attacker. Bahkan dalam SOC log menjadi komponen penting sebagai bahan yang digunakan SIEM untuk mengkorelasi data dari berbagai sumber. Tugas kita hanya memastikan setiap program penting mencatat setiap aktivitas (logging) dan menyimpannya dengan benar. contoh: SSH menulis file log kedalam **/var/log/auth.log**.

### 4. Menggunakan firewall

Firewall berfungsi sebagai pengatur lalu lintas jaringan yang keluar masuk sistem. Dengan firewall kita dapat memblokir koneksi yang tidak diinginkan dan hanya mengizinkan koneksi yang sah sesuai dengan rules yang sudah dibuat. contoh firewall dasar pada linux yang dapat kita gunakan dengan mudah yaitu Uncomplicated Firewall (UFW)

### 5. Membatasi hak akses

Dalam linux setiap user memiliki 3 hak akses utama yang dapat ditentukan yaitu Read (R), Write (W), dan Execute (X). semakin tinggi hak akses pada program penting maka semakin besar juga resiko yang dapat ditimbulkan saat user terkena kompromi. Dengan hak akses tinggi yang tidak dikonfigurasi dengan baik attacker mendapat jalur emas untuk menguasai sistem. Oleh karena itu, kita harus membatasi dan mengaudit hak akses setiap user seketat mungkin untuk meminimalkan resiko.

## Kesimpulan
  
Hardening adalah proses yang sangat penting untuk menguatkan keamanan sistem khususnya linux. Dengan ini kita dapat menimalisir resiko yang dapat ditimbulkan dan memperkecil attack vector serta membatasi gerak gerik attacker.          
