# Memory Forensic

<p align='center'>
  <img src='assets/img/ram.jpg' width='400'>
</p>

Memory forensic adalah cabang digital forensik dengan fokus pada analisis memori volatil seperti RAM untuk menemukan artifak bukti yang tidak tersimopan permanen pada disk atau media penyimpanan non-volatil.

## Apa yang dicari dalam proses memory forensic ?

1. Proses Aktif

Melihat proses, program atau aplikasi apa saja yang sedang berjalan, termasuk malicious process dan malware. Ini tidak dapat ditemukan pada disk forensic karena proses atau program hanya berjalan saat komputer sedang menyala.

2. Network Connections (Socket)

Informasi jaringan aktif (IP address, port, state, dll) berguna untuk mendeteksi backdoor atau c2. Malware yang menggunakan c2 hanya bisa dilihat saat komputer seddang menyala.

3. Artifak Malware (IoC)

Beberapa diantaranya:

- Injeksi kode mencurigakan
- Rootkit yang sedang berjalan
- Perintah mencurigakan yang dieksekusi

4. Kredensial dan Key sementara

Mencari password, token, atau enkripsi yang disimpan sementara pada RAM. Contoh: Beberapa jenis ransomware menyimpan key sementara pad ram, hal ini memungkinkan proses dekripsi tanpa harus membayar pada pelaku.

*Kenapa memory forensic penting?*

- Banyak malware modern tidak meninggalkan jejak pada disk (fileless).
- RAM dapat memperlihatkan kondisi sistem yang sebenarnya saat insiden terjadi.
- Informasi di memori sering lebih lengkap dibanding hanya melihat disk. 
