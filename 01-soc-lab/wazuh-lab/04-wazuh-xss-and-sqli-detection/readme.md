# XSS and SQLI detection with wazuh

Wazuh sebagai SIEM akan mengumpulkan berbagai macam log termasuk dari service seperti nginx atau apache dan mencari serta mencocokan signature tertentu berdasarkan rules. Oleh karena itu wazuh dapat mendeteksi percobaan cross site scripting (xss) dan sql injection (sqli) pada web berdasarkan rules yang telah dibuat. hal ini sangat berguna bagi tim SOC untuk mengambil tindakan cepat dan mengevaluasi keamanan web. 

## Deteksi XSS dan SQLi

Pada dasarnya wazuh telah mempunyai rules default untuk mendeteksi payload yang dimasukan attacker seperti xss dan sqli, namun ketika penginstallan pertama wazuh alert yang muncul hanya yang berlevel 7 atau lebih karena konfigurasi bawaan pada *ossec.conf*, sementara rules xss dan sqli mempunyai level 5 by default. Jadi kita harus menurunkan batas level untuk memunculkan alert atau menaikan level rules xss dan sqli itu sendiri.

![gambar rules](assets/img/rules-xss-sqli)

