# Wazuh and suricata integration

<p align="center">
  <img src="assets/img/suricata.jpg" width="300">
</p>

Suricata merupakan IDS (intrusion detection system) yang dikembangkan OISF. Dirancang untuk mendeteksi ancaman secara real-time yang dapat menganalisis lalu lintas jaringan dengan kecepatan tinggi berkat sistem multi-threading nya. Suricata banyak digunakan di organisasi dan industri saat ini, dengan basis open source dan mudah diintegrasikan dengan tools lain seperti SIEM menjadikan suricata banyak digemari di kalangan blue team.

## Integrasi dengan wazuh

Mengintegrasikan suricata dengan wazuh bertujuan untuk membangun sistem deteksi ancaman yang lebih komprehensif dengan menggabungkan kemampuan Intrusion detection system (IDS) dari suricata dan Security information and event management (SIEM) milik wazuh. mengintegrasikan suricata dengan wazuh terbilang cukup mudah dilakukan karena memang keduanya sudah mendukung environment masing masing.

## Langkah-langkah

1. Menginstall suricata pada mesin yang akan dijadikan sebagai IDS di sini saya gabungkan dengan agent wazuh karena saya hanya menggunakan dua mesin 
```bash
sudo apt install suricata -y
```
2. Biasanya akan ada tampilan untuk setup jaringan yang ingin dipantau atau bisa kita set di */etc/suricata/suricata.yaml*

3. Pada bagian HOME_NET baris pertama bisa di setting dan disesuaikan dengan jaringan yang ingin dipantau oleh suricata

4. Setelah itu selesai penginstallan suricata lanjut ke setup wazuh-agent agar dapat memantau jaringan pada suricata

5. Masuk ke */var/ossec/etc/ossec.conf* pada wazuh-agent dan tambahkan baris baru di dalam tag <ossec_config> paling bawah, penting!!! suricata menghasilkan dua log di */var/log/suricata/* yaitu *eve.json* dan *fast.log*. Perbedaan keduanya adalah pada informasi yang diberikan *fast.log* hanya memebrikan informasi ringkas tentang alert yang dimunculkan, sementara *eve.json* memebrikan informasi detail terkait alert dan ini yang biasa digunakan karena dapat memebri informasi full pada dashboard wazuh.  
```bash
<ossec_config>

  <local_file>
    <log_format>json</log-format>
    <location>/var/log/eve.json</location> # arahkan ke path log suricata 
  </local_file>
  
</ossec_config>
```
6. Restart wazuh-agent
```bash
sudo systemctl restart wazuh-agent
```
7. Setelah itu bisa tes alert dengan command dan lihat pada dashboard wazuh 
```bash
curl https://testmynids.org/uid.index.html
```

