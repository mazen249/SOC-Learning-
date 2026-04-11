# 🛡 Investigation 1 - Malicious Web Activity

## 📌 Scenario
Suspicious activity detected from external IP targeting a web server.

---

## 🌐 Target IP
198.51.100.55

---

## 📊 Total Requests

![Total Requests](screenshots/total-requests.png)

The IP generated 7876 requests, which is abnormally high and indicates automated activity.

---

## 📋 Raw Log Analysis

![Raw Logs](screenshots/raw-logs.png)

Initial log inspection shows repeated requests from the same IP interacting with multiple endpoints using GET and POST methods.

---

## 🔍 Suspicious Paths Analysis

![Suspicious Paths](screenshots/paths.png)

Multiple malicious endpoints were identified:

- /download?file=../../etc/passwd → Path Traversal  
- /item.php?id=1 AND SLEEP(5)-- → SQL Injection  
- /search.php?q=test' AND SLEEP(5)-- → SQL Injection  
- /shell.php?cmd=whoami → Command Execution (RCE)  
- /.env and /.git/config → Sensitive data exposure  

This confirms active exploitation attempts.

---

## 📡 Response Status Analysis

![Status Codes](screenshots/status.png)

Observed HTTP responses:

- 200 → Successful requests (⚠️ indicates some attacks succeeded)
- 403 → Blocked attempts
- 404 → Enumeration/scanning behavior
- 500 / 504 → Server errors during attack

---

## 🧠 Findings

- High volume of requests from a single IP
- Evidence of:
  - SQL Injection
  - Path Traversal
  - Remote Command Execution (RCE)
  - Sensitive file access attempts
- Mixed response codes indicate both blocked and successful attacks

---

## 🚨 Conclusion

The activity represents a multi-stage web application attack involving reconnaissance and exploitation techniques.

The presence of HTTP 200 responses suggests that some malicious requests were successfully processed by the server.

---

## 🔴 Severity
High

---

## 🛠 Tools Used
- Splunk
- TryHackMe Lab
