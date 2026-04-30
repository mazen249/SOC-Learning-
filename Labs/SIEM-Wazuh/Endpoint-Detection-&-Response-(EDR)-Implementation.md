# 🛡 Building a Security Monitoring Lab with Wazuh & Docker

## 📌 Overview

In this lab, I built a complete security monitoring environment using Wazuh and Docker.

The objective was to simulate a real SOC environment by deploying a SIEM solution and connecting an endpoint for monitoring and detection.

---

## 🏗 Lab Setup

- Installed Docker on Windows  
- Deployed Wazuh using Docker (PowerShell)  
- Successfully initialized Wazuh services  

📸 Docker :
![Setup](./images/s1.png)

📸 Wazuh Deployment:
![Deployment](./images/s2.png)
![Deployment](./images/s3.png)

---

## 💻 Endpoint Integration

- Installed Wazuh agent on Kali Linux  
- Configured agent to connect to Wazuh server  
- Successfully registered the endpoint  

📸 Agent Configuration (Kali):
![Kali Agent](./images/s4.png)

📸 Agent Added to Wazuh:
![Agent Added](./images/s5.png)

📸 Final Agent Registration:
![Agent Registered](./images/s7.png)

---

## 🔍 Monitoring & Visibility

After connecting the endpoint, Wazuh dashboard was used to monitor:

- System activity  
- Security events  
- Endpoint status  

This demonstrates how SOC analysts gain visibility over connected systems.

---

## 🧠 Key Learnings

- Understanding how SIEM (Wazuh) works  
- Deploying security tools using Docker  
- Connecting endpoints using agents  
- Monitoring systems in a centralized dashboard  

---

## 🎯 Conclusion

This lab provided hands-on experience in building a SOC monitoring environment and understanding how security teams monitor endpoints and detect suspicious activity.

It represents a foundational step toward working as a SOC Analyst.
