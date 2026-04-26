# 🧰 Splunk Cheat Sheet - SOC Learning

## 📌 Overview
This document contains the main SPL queries and techniques I used during my SOC investigations using Splunk.

---

# 🔍 Basic Search

## Show all data
index=main

## Show limited results
index=main | head 10

---

# 📊 Data Exploration

## View all available fields
index=main | table *

## Filter specific data
index=main clientip=95.103.151.244

---

# 🌐 IP Analysis

## Count events by IP
index=main | stats count by clientip

## Sort IPs by highest activity
index=main 
| stats count by clientip 
| sort - count

---

# 🔍 URI / Path Analysis

## Most requested paths
index=main 
| stats count by uri_path 
| sort - count

## Analyze specific IP behavior
index=main clientip=95.103.151.244
| stats count by uri_path

---

# 📡 Status Code Analysis

## Count responses by status
index=main 
| stats count by status

## Analyze status for specific IP
index=main clientip=95.103.151.244
| stats count by status

---

# 🤖 User-Agent Analysis

## Identify tools or bots
index=main 
| stats count by useragent

## Check user agent for specific IP
index=main clientip=66.249.72.235
| stats count by useragent

---

# 🚨 Suspicious Activity Detection

## Search for possible attacks
index=main 
uri_path="*passwd*" OR uri_path="*cmd*" OR uri_path="*sleep*" OR uri_path="*select*"

## Advanced suspicious search
index=main
| search uri_path="*passwd*" OR uri_path="*shadow*" OR uri_path="*cmd*" OR uri_path="*whoami*" OR uri_path="*select*" OR uri_path="*sleep*"
| stats count by clientip
| sort - count

---

# 🧠 Key Concepts Learned

- Logs contain user and system activity
- Not all high traffic is malicious
- Bots like Googlebot and YandexBot are normal
- Attacks are identified by behavior, not volume
- Always validate findings before concluding

---

# 🛠 Tools Used

- Splunk

---

# 🎯 Goal

To develop practical SOC analysis skills including:
- Log analysis
- Threat detection
- Investigation documentation
