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

