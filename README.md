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
### 1. Attack Simulation (Red Team)
<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/04d79c76-5693-4ad9-8659-37e91ac808af" />


### 2. SIEM Threat Hunting Dashboard
<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/ece795f3-8c33-4dda-9efe-71665a78007f" />


### 3. Security Event Log Breakdown
<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/0317b9b5-f312-4351-a959-61148c159675" />

### 4. IT Hygiene & System Overview
<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/27c4314d-f91f-4446-8c43-ab8905b95297" />

🛠️ Skills Demonstrated
 Deployment and Configuration of XDR/SIEM Agents.
 Log Ingestion, Event Parsing, and Alarm Generation.
 Operationalizing the MITRE ATT&CK framework for Threat Hunting.
 Identifying Network Security Controls (Active Firewall Drop vs. Log Generation).
 Forensic Analysis of Windows Authentication Failures.
