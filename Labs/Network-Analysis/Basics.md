# 🛡 Network Traffic Analysis (NTA)

## 📌 Overview
This section summarizes the fundamentals of Network Traffic Analysis (NTA), including data sources, traffic capture methods, and analysis techniques used in SOC environments.

---

## 🎯 What is NTA?
Network Traffic Analysis is the process of monitoring, capturing, and analyzing network data to detect suspicious activity, investigate incidents, and understand network behavior.

---

## 🚀 Why is NTA Important?

- Detect malicious or abnormal activity  
- Reconstruct attacks during incident response  
- Validate security alerts  
- Identify:
  - Data Exfiltration  
  - Command & Control (C2)  
  - DNS Tunneling  

---

## 📦 Data Sources

### 1️⃣ Logs
Logs provide high-level information about network activity.

Examples:
- Windows Event Logs  
- Apache Web Logs  
- SSH Logs  

Pros:
- Easy to access  
- Fast to analyze  

Cons:
- Limited visibility  
- No full packet details  

---

### 2️⃣ Full Packet Capture (PCAP) 🔥
Captures complete network traffic including headers and payload.

Advantages:
- Full visibility into traffic  
- Deep analysis capability  

Capture Methods:
- Network TAP (hardware-based)  
- Port Mirroring (SPAN)

---

### 3️⃣ Network Statistics

Protocols:
- NetFlow  
- IPFIX  

Provides:
- Source and destination  
- Traffic volume  
- Communication patterns  

Limitation:
- No payload visibility  

---

## 🧠 TCP/IP Layers in Analysis

### 🔹 Application Layer
- HTTP (GET / POST)  
- DNS Queries  

---

### 🔹 Transport Layer
- TCP / UDP  
- Ports  
- Flags (SYN, ACK)

---

### 🔹 Internet Layer
- IP Address  
- TTL  
- Fragmentation  

---

### 🔹 Link Layer
- MAC Address  
- ARP  

---

## 🌐 Key Protocols

### 🔸 DNS
- Resolves domain names to IP addresses  
- Can be abused (DNS Tunneling)

---

### 🔸 SMB + Kerberos
- Kerberos → Authentication (Tickets)  
- SMB → File sharing  

---

### 🔸 TLS
- Encrypts communication (HTTPS)  
- Ensures confidentiality and integrity  

---

## ⚙️ Traffic Capture Methods

### 🔹 Network TAP
- Hardware device  
- Copies all traffic  
- No performance impact  

---

### 🔹 Port Mirroring (SPAN)
- Configured on switches  
- Copies traffic to monitoring port  
- May impact performance  

---

## 🛠 Tools

- Wireshark 🔥  
- tcpdump  
- Suricata / Snort / Zeek  

---

## 📊 Network Statistics Analysis

Used to detect:

- Command & Control (C2)  
- Data Exfiltration  
- Lateral Movement  

---

## 🔑 Key Takeaways

- Logs provide limited visibility  
- Packet capture provides full visibility  
- NetFlow provides behavioral insights  
- Combining all sources = effective analysis  

---

## 🧠 Personal Notes

- Packet analysis is the deepest level of investigation  
- Understanding protocols is critical for SOC analysts  
- Wireshark is a core tool for traffic analysis  

---
