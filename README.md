# 🔐 Brute Force Detection using Wazuh

## 📌 Overview
This project demonstrates detection of SSH brute force attacks using **Wazuh SIEM**.  
A simulated attack was performed from **Kali Linux** using **Hydra**, and custom Wazuh rules were created to detect multiple failed login attempts in real-time.

---

## 🛠 Tools Used
- **Wazuh SIEM** – Security monitoring and alerting  
- **Kali Linux** – Attack simulation platform  
- **Hydra** – Brute force tool  
- **Windows 11** – OpenSSH server as target  

---

## 🚀 Features
- Detection of multiple failed SSH login attempts  
- Real-time correlation using **frequency and timeframe**  
- Custom Wazuh rule creation  
- MITRE ATT&CK mapping: **T1110 – Brute Force**  
- Dashboard visualization in Wazuh  

---

## 🧪 Attack Simulation

### 🔹 Attack Steps
1. Start SSH server on Windows 11.  
2. From Kali Linux, run Hydra to attempt brute force on the SSH service.  

### 🔹 Hydra Command Used
```bash
hydra -l lap11 -P bpaas.txt ssh://192.168.1.10 -t 1 -W 10 -V
