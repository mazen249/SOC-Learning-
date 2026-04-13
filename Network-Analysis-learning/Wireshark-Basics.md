# 🧠 Network Traffic Analysis (NTA) & Wireshark Basics

## 📌 Overview
This module covers the fundamentals of Network Traffic Analysis (NTA) and practical usage of Wireshark to inspect and analyze network traffic at different layers of the TCP/IP model.

---

## 🎯 Objectives
- Understand why network traffic analysis is important
- Learn how network communication works (DNS, HTTP, TCP/IP)
- Analyze packets using Wireshark
- Extract useful data from PCAP files
- Detect suspicious or malicious activity

---

## 🌐 Why Network Traffic Analysis?

Network traffic analysis helps to:

- Detect malicious activity (e.g., C2 communication, data exfiltration)
- Investigate incidents and reconstruct attacks
- Validate alerts from SIEM tools
- Monitor abnormal behavior in the network

---

## 🧱 TCP/IP Layers (What to Analyze)

### 1️⃣ Application Layer
- Protocols: HTTP, DNS, SMB
- Important fields:
  - HTTP methods (GET, POST)
  - Headers (User-Agent, Host)
  - Payload (files, HTML, commands)

---

### 2️⃣ Transport Layer
- Protocols: TCP / UDP
- Important fields:
  - Ports (source/destination)
  - Flags (SYN, ACK, PSH)
  - Sequence numbers (Seq)
  - Window size (Win)

📌 Used for detecting:
- Session hijacking
- Suspicious connections

---

### 3️⃣ Network Layer
- Protocol: IP
- Important fields:
  - Source/Destination IP
  - TTL
  - Fragmentation

---

### 4️⃣ Data Link Layer
- MAC addresses
- Used in detecting:
  - ARP spoofing
  - MAC anomalies

---

## 🌐 DNS Tunneling (Attack Concept)

- Attacker uses DNS queries to communicate with C2 server
- Uses:
  - Random subdomains
  - TXT records for commands

📌 Example:aj39skdm.malicious.com

---

## 🔐 HTTP Analysis

### Request Example:GET /file.zip HTTP/1.1
User-Agent: curl/7.85.0

### Response Example:HTTP/1.1 200 OK
Content-Type: application/zip

📌 Logs show headers only, but NOT payload  
👉 Need packet analysis to see actual content

---

## 🧰 Wireshark Basics

### Key Features:
- Packet capture & analysis
- Protocol inspection
- Filtering traffic
- Extracting files

---

## 🔍 Important Skills Learned

### 1️⃣ Packet Inspection
- Analyze layers:
  - Frame
  - MAC
  - IP
  - TCP
  - Application

---

### 2️⃣ Following StreamsFollow → TCP Stream
👉 Reconstruct full communication

---

### 3️⃣ Filtering Traffic
Examples:http
dns
tcp.port == 80

---

