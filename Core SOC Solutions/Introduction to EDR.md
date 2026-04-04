# 🛡️ Endpoint Detection and Response (EDR) – Summary

---

## 📌 Overview

EDR is an advanced security solution that monitors, detects, and responds to threats at the endpoint level. Unlike traditional Antivirus, EDR focuses on **behavior**, not just signatures.

---

## 🧠 Key Concepts

### 1. EDR vs Antivirus

| Feature | Antivirus | EDR |
|---------|-----------|-----|
| Detection | Signature-based | Behavior + Anomaly + IOC + ML |
| Visibility | Low | Full telemetry |
| Response | Quarantine file | Isolate, terminate, remote access, collect artefacts |

---

### 2. EDR Architecture

| Component | Function |
|-----------|----------|
| **Agent (Sensor)** | Installed on each endpoint, collects telemetry |
| **Console** | Centralized platform for analysis and response |

---

### 3. Telemetry (Data Collected)

| Type | What it captures |
|------|------------------|
| Process Executions | Running and terminated processes, parent-child relationships |
| Network Connections | Outbound connections, IPs, ports |
| Command Line Activity | Commands executed in CMD, PowerShell |
| Files & Folders | Modifications, creations, deletions |
| Registry | Changes to Windows configuration settings |

---

### 4. Detection Techniques

| Technique | Description |
|-----------|-------------|
| **Behavioral Detection** | Flags unusual parent-child relationships (e.g., winword.exe spawning powershell.exe) |
| **Anomaly Detection** | Flags deviation from normal endpoint behavior |
| **IOC Matching** | Matches hashes, IPs, domains with threat intelligence |
| **MITRE ATT&CK Mapping** | Maps activity to tactics and techniques |
| **Machine Learning** | Detects complex patterns (e.g., fileless malware) |

---

### 5. Response Actions

| Action | Use Case |
|--------|----------|
| **Isolate Host** | Compromised endpoint trying to move laterally |
| **Terminate Process** | Malicious process on critical system |
| **Quarantine** | Malicious file (preserve for analysis) |
| **Remote Access (RTR)** | Custom actions not supported by EDR |
| **Artefacts Collection** | Forensics (memory dump, logs, registry) |

---

## ✅ Summary

- EDR provides **full visibility** into endpoint activity
- **Telemetry** is the foundation of detection and investigation
- **Behavioral analysis** catches attacks that AV misses
- **MITRE ATT&CK** helps classify threats by tactic and technique
- SOC analysts use EDR for **triage, investigation, and response**
