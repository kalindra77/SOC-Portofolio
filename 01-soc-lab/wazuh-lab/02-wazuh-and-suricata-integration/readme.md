# Wazuh and suricata integration

<p align="center">
  <img src="../assets/suricata.jpg" width="300">
</p>

Suricata merupakan IDS (intrusion detection system) yang dikembangkan OISF. Dirancang untuk mendeteksi ancaman secara real-time yang dapat menganalisis lalu lintas jaringan dengan kecepatan tinggi berkat sistem multi-threading nya. Suricata banyak digunakan di organisasi dan industri saat ini, dengan basis open source dan mudah diintegrasikan dengan tools lain seperti SIEM menjadikan suricata banyak digemari di kalangan blue team.

## Integrasi dengan wazuh

Saya akan melakukan integrasi suricata dengan wazuh sebagai salah satu upaya enrichment data kemanan dari log yang dihasilkan suricata dan ditampilkan di wazuh dashboard
