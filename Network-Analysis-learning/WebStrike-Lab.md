# 🛡️ WebStrike Lab - Network Traffic Analysis (SOC Level 1)

## 🔍 Overview
This project demonstrates a network forensic investigation using Wireshark to analyze a potential web server compromise.  
The objective was to identify suspicious activity, analyze attacker behavior, and extract key indicators of compromise (IOCs).

---

## 🧰 Tools Used
- Wireshark
- IP Geolocation Tool
- HTTP Analysis

---

## 🧠 Step 1: Filter HTTP Traffic

I started by filtering HTTP traffic to focus on web-based communication:

http

📸 Screenshot:  
![HTTP Filter](/imge/http.png)

---

## 🌍 Step 2: Identify Suspicious IP

I identified a suspicious IP address from the traffic and investigated it using an IP lookup tool.

- Suspicious IP: 117.11.88.124
- Location: Tianjin, China

📸 Screenshot:  
![IP Lookup](/imge/ip.png)

---

## 🧾 Step 3: Analyze User-Agent

Next, I inspected the HTTP headers to identify the User-Agent used in the communication.

- User-Agent: Mozilla/5.0 (Linux x86_64, Firefox)

📸 Screenshot:  
![User Agent](/imge/user.png)

---

## 📤 Step 4: Analyze POST Requests

To identify data being sent to the server, I filtered POST requests:

http.request.method == "POST"

This revealed suspicious upload activity.

📸 Screenshot:  
![POST Request](/imge/post.png)

---

## 📁 Step 5: Identify Uploaded Malicious File

I found that the attacker uploaded a suspicious file:

- File name: image.jpg.php
- This indicates a possible web shell upload

📸 Screenshot:  
![Malicious Upload](/imge/php.png)

---

## 🎯 Step 6: Attacker Accessing the File

The attacker attempted to access the uploaded file:

/reviews/uploads/image.jpg.php

📸 Screenshot:  
![File Access](/imge/access.png)

---

## 🗂️ Step 7: Identify Upload Directory

The server stores uploaded files in the following directory:

/reviews/uploads/

📸 Screenshot:  
![Upload Directory](/imge/upload.png)

---

## 🚨 Findings (IOCs)

- Suspicious IP: 117.11.88.124  
- Malicious File: image.jpg.php  
- Upload Endpoint: /reviews/upload.php  
- File Path: /reviews/uploads/  
- Attack Type: Web Shell Upload  

---

## 🧩 Conclusion

The analysis confirms that the attacker successfully uploaded a malicious PHP file (web shell) to the server and attempted to execute it.  
This indicates a file upload vulnerability that was exploited.

---

## 📌 Skills Demonstrated

- Network Traffic Analysis  
- Wireshark Filtering  
- HTTP Inspection  
- Threat Detection  
- Basic Incident Investigation  

---
