# Wazuh

<p align="center">
  <img src="assets/img/wazuh.jpg" width="300">
</p>

Wazuh adalah platform keamanan open-source yang dirancang untuk membantu organisasi dalam mendeteksi ancaman, memantau integritas sistem, serta memastikan kepatuhan terhadap kebijakan dan regulasi keamanan. Dengan kemampuan yang luas, Wazuh mengintegrasikan fitur seperti deteksi intrusi, analisis log, pemantauan file, serta manajemen kerentanan, sehingga memberikan visibilitas penuh terhadap kondisi keamanan infrastruktur TI. Selain itu, Wazuh dapat berintegrasi dengan berbagai alat lain seperti Elasticsearch, Kibana, dan Splunk, menjadikannya solusi yang fleksibel dan kuat untuk kebutuhan keamanan siber modern.

Selain itu, komunitas wazuh sudah sangat besar dan terus berkembang, faktor utamanya adalah karena basis open-source nya yang menjadikan wazuh digemari banyak orang. Fitur yang diberikan pun cukup lengkap seperti Threat intelligence, File Integrity monitoring, Vulneberallity detection hingga endpoint security seperti malware detection dan configuration assesment serta masih banyak lagi. Dengan segala fiturnya wazuh dapat menjadi salah satu pilihan platform yang minim biaya dan dapat diandalkan

| Project | Deskripsi
|----------|------------|
| [Setup Custom Rules](01-setup-custom-rules-wazuh) | Membat custom rules wazuh untuk menghindari false-positive
| [Wazuh & Suricata Integration](02-wazuh-and-suricata-integration) | Mengintegrasikan wazuh dengan suricata sebagai IDS
| [SSH Brute-Force Detection](03-wazuh-ssh-brute-force-detection) | Mendeteksi percobaan login berulang sebagai Brute-Force attack  
| [XSS and SQLI Detection](04-wazuh-xss-and-sqli-detection) | Mendeteksi input user pada website yang mengandung payload xss dan sqli
| [File Integrity Monitoring](05-wazuh-file-integrity-monitoring) | Setup fitur File Integrity monitoring (FIM) pada wazuh 
