# 🛡️ SOC Automation & Advanced Threat Detection Lab  
(Wazuh SIEM + Sysmon + Shuffle SOAR)

---

## 📌 Overview

This project demonstrates building a modern SOC environment that covers the full attack lifecycle:

➡️ Detection → Analysis → Automated Response  

The lab focuses on detecting Credential Access attacks (Mimikatz) and handling Defense Evasion techniques such as file renaming.

---

## 🧱 Architecture

The lab simulates real-world log flow:

- 🖥 Windows 10 Endpoint (Sysmon enabled)  
- 🧩 Wazuh Agent  
- 📊 Wazuh Manager (Docker)  
- ⚡ Shuffle SOAR (Automation Layer)  

📸  
![Architecture](./images/s1.png)

---

## ⚙️ Implementation

### 🔹 1. Wazuh Agent Setup

Connecting Windows machine to Wazuh server:

📸  
![Agent Setup](./images/s2.png)

---

### 🔹 2. Editing Configuration Files

Modifying configuration files (ossec.conf / agent settings):

📸  
![Config Edit](./images/s3.png)

---

### 🔹 3. Wazuh Dashboard Verification

Verifying agent connection and status:

📸  
![Dashboard](./images/s4.png)

---

### 🔹 4. Log Collection Testing

Testing log flow and confirming data ingestion:

📸  
![Logs Test](./images/s5.png)

---

### 🔹 5. Deep Log Analysis

Inspecting raw logs for detailed visibility:

📸  
![Deep Logs](./images/s6.png)

---

## 🔧 Configuration

### 🔹 1. Custom Detection Rules

Creating rules to detect suspicious behavior:

📸  
![Rules](./images/s7.png)

---

### 🔹 2. Sysmon Deployment

Installing Sysmon for enhanced monitoring:

📸  
![Sysmon](./images/s8.png)

---

## 💣 Attack Simulation

### 🔹 1. Mimikatz Execution

Simulating credential dumping attack:

📸  
![Mimikatz](./images/s9.png)

---

### 🔹 2. Additional Attack Validation

Extra validation/testing during attack phase:

📸  
![Attack Validation](./images/s10.png)

---

## 🚨 Detection & Results

### 🔹 1. Event Viewer Logs

Monitoring logs from Windows Event Viewer:

📸  
![Event Viewer](./images/s11.png)

---

### 🔹 2. SIEM Detection Output

Viewing alerts and detections inside Wazuh:

📸  
![SIEM Detection](./images/s12.png)

---

### 🔹 3. Rule Trigger Evidence

Proof of detection via custom rule:

📸  
![Rule Trigger](./images/s13.png)

---

## ⚡ Automation (Shuffle SOAR)

### 🔹 1. Integration Configuration

Setting up Wazuh → Shuffle integration:

📸  
![Integration Config](./images/s14.png)

---

### 🔹 2. Shuffle Workflow

Automation workflow inside Shuffle:

📸  
![Shuffle Workflow](./images/s15.png)

---

## 🎯 Key Achievements

- ✅ Built a SOC lab (SIEM + SOAR)  
- ✅ Integrated Wazuh with Shuffle automation  
- ✅ Detected credential dumping attacks  
- ✅ Bypassed attacker evasion techniques  
- ✅ Created custom detection rules  
- ✅ Mapped attack to MITRE ATT&CK (T1003)  
- ✅ Advanced SIEM Debugging (fixed integratord issues)  
- ✅ Linux-Docker interoperability handling  

---

## 🛠 Technical Challenges (Debugging Journey)

### 🔹 XML Structure Complexity

The wazuh-integratord module failed due to XML structure issues.

✔ Fixed by restructuring ossec.conf

---

### 🔹 Docker Environment Constraints

✔ Problem:
- CRLF vs LF formatting  

✔ Solution:
- Used printf to ensure correct Linux format  

---

### 🔹 Process Debugging

Used:
wazuh-integratord -dd

✔ Result:
- Fixed integration issues  
- Restored service  

---

## 🏁 Conclusion

This lab demonstrates a full SOC pipeline:

- 🔍 Sysmon → Visibility  
- 🧠 Wazuh → Detection  
- ⚡ Shuffle → Automation  

➡️ Result: Real-world capable threat detection & response system

- 🔍 Sysmon (Visibility)  
- 🧠 Wazuh (Detection)  
- ⚡ Shuffle (Automation)  

➡️ The environment demonstrates a complete Detection → Response pipeline capable of handling advanced threats.
