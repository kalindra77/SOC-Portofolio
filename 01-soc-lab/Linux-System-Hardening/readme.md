# Linux System Hardening

<p align="center">
  <img src="/assets/img/linux.jpeg" width="400">
</p>

Hardening sistem berarti mengunci, memperkuat, atau meminimalkan permukaan serangan sehingga dapat menghambat attacker saat menjalankan aksinya. Menghapus software yang tidak diperlukan, Mengonfigurasi default values ke pengaturan seketat mungkin, dan Menjalankan hanya apa yang kita butuhkan secara eksplisit. Contoh dalam kehidupan sehari-hari, Sebuah toko perhiasaan akan menggunakan keamanan ekstra saat sedang tutup malam hari entah dengan kunci besar dan lebih kuat atau bahkan dengan menaruh seorang security guard disana, tujuannya tak lain adalah meminimalkan resiko dan mengurangi permukan serangan yang dapat dilakukan oleh pencuri.

## Mengapa Hardening Penting ?

Siapa pun yang menjalankan infrastuktur sistem komputer apalagi mengelola dan menyimpan data penting mesti khawatir terhadap keamanan sistemnya. Sesuai dengan salah satu prinsip cybersecurity yang tidak tertulis yaitu: "No system is safe" Tidak ada sistem yang aman, bahkan sekuat-kuatnya infrastukur keamanannya attacker selalu mempunyai cara dan celah yang dapat digunakan. Dalam peraturan pemerintah setiap negara, kebocoran data atau pelanggaran privasi pelanggan baik disengaja maupun tidak memiliki hukuman atau konsekuensi tertentu seperti denda atau pencabutan izin operasi, belum lagi tercorengnya reputasi organisasi tersebut yang makin memperburuk dampaknya.

## 10 Langkah Hardening

Saya akan memberi 10 langkah hardening linux, tentu ini bukan hardening lengkap karena menyesuaikan dengan perangkat yang saya gunakan namun ini merupakan langkah awal yang mungkin perlu diterapkan. DISCLAIMER!: Saya menggunakan distro Ubuntu sehingga mungkin akan berbeda prosesnya dengan distro lain.

### 1. Pastikan sistem selalu up-to-date

Ini hal yang sering disepelekan namun sangat fatal jika tidak dilakukan

  

