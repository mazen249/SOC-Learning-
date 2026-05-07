<h1 align="center">🛡 SOC Learning Portfolio</h1>
<h3 align="center">Hands-on Labs & Security Investigations</h3>

<p align="center">
<img src="https://img.shields.io/badge/-SOC%20Operations-0A66C2?&style=for-the-badge" />
<img src="https://img.shields.io/badge/-Threat%20Detection-FF0000?&style=for-the-badge" />
<img src="https://img.shields.io/badge/-Incident%20Response-000000?&style=for-the-badge" />
<img src="https://img.shields.io/badge/-AI%20Automation-FFD700?&style=for-the-badge" />
</p>

---

## 📌 Overview

labs focused on Detection Engineering, Incident Response, and Threat Analysis. My investigations follow industry-standard frameworks such as the Cyber Kill Chain and MITRE ATT&CK to ensure comprehensive analysis.

Each lab includes:

 - Step-by-step analysis of real-world attack scenarios.

 - Technical findings derived from log and traffic examination.

 - Remediation conclusions to mitigate future security risk

---


## 🚀 Projects Portfolio (The 14 Strategic Labs)

| # | Project Name | The "Magic" Description (Professional Skills Acquired) | Status & Link |
| :--- | :--- | :--- | :--- |
| **01** | **📊 SIEM Log Monitoring** | Built Splunk SIEM lab to ingest and analyze Sysmon/Windows logs; created custom detection rules for brute force and PowerShell-based attacks. | [📂 View](./Labs/SIEM-Splunk/) |
| **02** | **📧 Simulated Phishing IR** | Simulated phishing attack in lab and performed full IR process including log review, malware identification, and executive-level reporting. | [📂 View](./Labs/Phishing-Investigation/) |
| **03** | **🌐 IDS & Packet Analysis** | Deployed Suricata/Snort IDS to monitor test network; generated attack traffic and tuned rules to reduce false positives and detect SQL injection attempts. | [📂 View](./Labs/Network-Analysis/) |
| **04** | **☁️ Cloud Monitoring** | Configured AWS CloudTrail/GuardDuty to detect and alert on suspicious IAM events including unauthorized access and S3 misconfigurations. | [⏳ Planning](#) |
| **05** | **🛡️ Endpoint Monitoring** | Ingested Sysmon logs into Wazuh and developed custom alert rules to detect credential dumping and persistence tactics (e.g., Mimikatz). | [📂 View](./Labs/SIEM-Wazuh/) |
| **06** | **🎯 Threat Hunting** | Performed threat hunt on Zeek and Windows log dataset; identified lateral movement and brute-force login indicators using SPL queries. | [⏳ Planning](#) |
| **07** | **🤖 SOC Automation** | Orchestrated a SOAR workflow using **Docker** to integrate **Wazuh & Shuffle**; developed scripts to enrich IOCs via VirusTotal API. | [📂 View](Labs/SIEM-Wazuh/Endpoint-Detection-&-Response-(EDR)-Implementation.md) |
| **08** | **🍯 Honeypot Lab** | Deployed SSH honeypot in cloud VM; captured and analyzed 5,000+ attacker attempts including common TTPs and password combos. | [⏳ Planning](#) |
| **09** | **📂 Threat Intel Research** | Compiled threat report on APT campaigns with enriched IOCs and MITRE TTP mapping; integrated with open-source MISP platform. | [⏳ Planning](#) |
| **10** | **📦 Malware Analysis** | Analyzed phishing email with malicious doc attachment; performed sandbox detonation and extracted PowerShell-based downloader behavior. | [⏳ Planning](#) |
| **11** | **🔍 WebStrike Lab** | Performed deep packet analysis of web-based attacks to identify Command and Control (C2) communication patterns. | [📂 View](./Labs/Network-Analysis/) |
| **12** | **🧪 Malware Traffic Analysis** | Investigated malicious network traffic to identify callback domains and extracted indicators of compromise (IOCs) from PCAP files. | [📂 View](Labs/Network-Analysis/Malware-Traffic-Analysis.md) |
| **13** | **🔐 Brute Force Investigation** | Analyzed Windows security event logs to detect and mitigate automated login attempts and credential stuffing attacks. | [📂 View](Labs/SEIM-Splunk/Screenshots/lockout.png) |
| **14** | **📥 PayPal Phishing Analysis** | Conducted real-world email header forensics and credential harvesting investigation to document adversary TTPs. | [📂 View](Labs/Phishing-Investigation/LetsDefend-Paypal-Phishing.md) |

---


## 🔍 Methodologies

- **Phishing Analysis:** Email forensics and sandbox detonation.
- **Network Forensics:** Packet analysis and IDS rule tuning.
- **Threat Hunting:** Anomaly detection using SPL/KQL and ATT&CK mapping.

📂 [Methodologies/](./Methodologies/)

---

## 🛠 Tools Used

<p>
<a href="https://www.wireshark.org/" target="_blank">
<img src="https://img.shields.io/badge/-Wireshark-1679A7?&style=for-the-badge&logo=Wireshark&logoColor=white" />
</a>

<a href="https://www.splunk.com/" target="_blank">
<img src="https://img.shields.io/badge/-Splunk-000000?&style=for-the-badge&logo=Splunk&logoColor=white" />
</a>

<a href="https://www.virustotal.com/" target="_blank">
<img src="https://img.shields.io/badge/-VirusTotal-394EFF?&style=for-the-badge" />
</a>

<a href="https://gchq.github.io/CyberChef/" target="_blank">
<img src="https://img.shields.io/badge/-CyberChef-FB8C00?&style=for-the-badge" />
</a>

<a href="https://wazuh.com/" target="_blank">
<img src="https://img.shields.io/badge/-Wazuh-005571?&style=for-the-badge" />
</a>

<a href="https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon" target="_blank">
<img src="https://img.shields.io/badge/-Sysmon-0078D6?&style=for-the-badge" />
</a>

<a href="https://shuffler.io/" target="_blank">
<img src="https://img.shields.io/badge/-Shuffle%20SOAR-FF6B00?&style=for-the-badge" />
</a>
</p>

---

## 🎯 Focus

Building strong practical skills in:

- Threat Detection  
- Incident Investigation  
- Security Monitoring  
- SOC Automation (SOAR)
