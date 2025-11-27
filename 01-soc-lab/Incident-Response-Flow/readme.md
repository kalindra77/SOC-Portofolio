# Incident Response Flow

<p align="center">
  <img src="assets/img/ir.png" width="400">
</p>

Incident-Response adalah proses yang terstruktur untuk mendeteksi, menangani, dan memulihkan sistem setelah terjadi insiden. Tujuan utamanya adalah meminimalkan kerusakan, memulihkan sistem secepat mungkin, dan mencegah insiden terulang kembali. 

## Tahap-Tahap Incident-Response

Dalam incident response ada 6 tahap alur utama yang menjadi standar penanganan. Tahap-tahap ini mencakup proses persiapan sebelum insiden hingga evaluasi setelah insiden. Tujuan alur ini adalah agar tim mendapat gambaran dan flow yang terstruktur sehingga dapat tetap tenang saat terjadi insiden.

### 1. Preparation (Persiapan)

Ini adalah tahap pertama sebelum terjadi insiden. Tujuan utama tahap ini adalah mempersiapkan segala sumber daya baik manusia maupun alat dan teknologi yang digunakan agar siap menghadapi insiden yang tak terduga. Contoh:

- Tuning dan setup SIEM, EDR, dan memastikan log tercatat lengkap
- Menetapkan SOP insiden secara jelas
- Latihan simulasi untuk menjaga dan melatih kesiapan tim

### 2. Identification (Identifikasi)

Tahap kedua saat terjadi insiden yaitu proses pengidentifikasian untuk memastikan insiden benar dan bukan false-positive. Dalam tahap seorang analyst sangat berperan untuk memastikan bahwa insiden adalah benar lalu menentukan prioritas serta klasifikasi insiden. Tahap ini juga bisa menjadi indikator kesiapan pada tools yang digunakan, misalkan jika banyak insiden ternyata false-positive maka mesti dilakukan tune-up pada alat yang digunakan. Contoh tahap ini:

- Alert pada SIEM / SOC 
- Menganalisa log, traffic jaringan, file, dan proses mencurigakan
- Triase level insiden : low/medium/high/crtical

### 3. Containment (Pembatasan)

Jika pada tahap dua dinyatakan insiden true-positive maka selanjutnya dilakukan tahap 3 yaitu Containment atau pembatasan. Proses ini bertujuan agar serangan tidak menyebar dan mengontaminasi sistem lain. Containment memiliki dua tipe:

a. Short-term Containment

Pencegahan dan pembatasan jangka pendek. contoh:

- isolasi host segera setelah insiden
- Blok koneksi keluar masuk menggunakan firewall atau arahkan ke sinkhole
- Kill proses tertentu

b. Long-term Containment

Pencegahan jangka panjang. Contoh:

- Mengganti kredensial yang terkompromi
- Patch celah yang dijadikan jalan masuk oleh attacker
- Menambah rules tambahan pada firewall atau IDS/IPS untuk jangka panjang

### 4. Eradication (Pembersihan)

Tahap ini sangat krusial untuk membersihkan sistem dari kontaminasi dan memastikan tidak dapat lagi diakses secara tidak sah oleh attacker. Attacker bisa saja memasukan malware yang sulit dideteksi seperti rookit, stealer canggih, ataupun celah zero-days yang bisa dimanfaatkan, oleh karena itu proses ini butuh keahlian yang solid dan proses yang serius. contoh:

- Menghapus malware yang terdeteksi
- Menghapus akses persisten attacker seperti key ssh atau cron yang dibuat
- Fix & patch celah yang menjadi pintu masuk

### 5. Recovery (Pemulihan)

Setelah diyakini sistem sepenuhnya bersih maka tahap selanjutnya adalah pemulihan pasca insiden ke kondisi normal. Tahap ini merupakan salah satu tujuan utama dalam proses penanganan insiden. Contoh:

- Restore layanan yang sempat dimatikan sementara
- Memulihkan akun akun yang sempat di disable
- Pemulihan kepercayaan jika menyangkut integritas dan nama baik organisasi

### 6. Lessons learned (Evaluasi)

Tahap yang sering dilupakan namun sangat krusial, Mengambil pelajaran dan evaluasi dari insidenyang terjadi. Contoh:

- Dokumentasi lengkap insiden
- Evaluasi tim dan semua sumber daya
- Update SOP 

## Kesimpulan

6 tahap standar penanganan insiden ini merupakan tahap yang sangat krusial dan wajib dipahami oleh tim keamanan dan organisasi. Tahap-tahap ini dapat meminimalkan resiko dan kerugian bagi organisasi yang terdampak insiden.   
    
