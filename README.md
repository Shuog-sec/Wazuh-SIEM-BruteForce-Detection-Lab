# 🛡️ Enterprise SIEM Deployment & Brute-Force Detection Lab (Wazuh & Kali Linux)

## 📌 Project Overview
This project demonstrates the deployment of an enterprise-grade **Wazuh SIEM (Security Information and Event Management)** solution to monitor, detect, and analyze real-time security events. The lab simulates a realistic cyber-attack scenario where a **Kali Linux** machine executes a **Brute-Force Attack (Password Guessing)** against a hardened **Windows 10 Enterprise** endpoint. The objective is to validate the capability of the SIEM platform to log, parse, and alert on malicious authentication behaviors mapped to global security frameworks.

---

## 🏗️ Lab Architecture & Topology
* **SIEM Server:** Wazuh Manager (Centralized Log Analytics & Alerts Dashboard)
* **Target Endpoint (Victim):** Windows 10 Enterprise (Monitored via Wazuh Agent)
* **Attacker Machine:** Kali Linux (Utilizing advanced password guessing tools)
* **Target Protocol:** SMB (Server Message Block) - Port 445

---

## ⚡ Active Defensive & Offensive Scenarios

### 1. Attack Simulation (Red Team)
To simulate a real-world credential stuffing attack, **Hydra** was deployed using a targeted wordlist to brute-force the Windows native `Administrator` account:
```bash
hydra -l Administrator -P /usr/share/wordlists/fasttrack.txt smb://10.0.2.7 -V -t 1



📊 Key Findings & SIEM Metrics
The Wazuh Manager successfully ingested and processed log data from the Windows host, yielding active defense results.
🛠️ Skills Demonstrated
 Deployment and Configuration of XDR/SIEM Agents.
 Log Ingestion, Event Parsing, and Alarm Generation.
 Operationalizing the MITRE ATT&CK framework for Threat Hunting.

---
![Image](https://github.com/user-attachments/assets/d444f828-121f-46a2-8e77-5bbf33748a6a)

![Image](https://github.com/user-attachments/assets/1f533718-5ef0-49ca-97b7-5c5a3884ef29)

![Image](https://github.com/user-attachments/assets/51d8d7c6-a18f-40d9-ba13-383376ef797d)

<img width="1280" height="960" alt="Image" src="https://github.com/user-attachments/assets/8f41c9e6-c1a1-4f25-9afd-a395f645884a" />


