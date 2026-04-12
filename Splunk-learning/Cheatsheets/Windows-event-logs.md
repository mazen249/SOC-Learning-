# 🪟 Windows Event Logs - SOC Notes

## 📌 Overview
Windows Event Logs record system and security activities on a Windows machine.  
They are essential for detecting attacks and suspicious behavior.

---

## 🔑 Important Event IDs

| Event ID | Description |
|----------|------------|
| 4624 | Successful login |
| 4625 | Failed login |
| 4634 | Logoff |
| 4672 | Admin privileges assigned |
| 4688 | Process creation |

---

## 🔍 Key Use Cases

### 🟥 Brute Force Detection
- Multiple Event ID 4625 from same IP
- Followed by Event ID 4624

➡️ Indicates attacker guessing passwords

---

### 🟡 Suspicious Login
- Login from unknown IP
- Login at unusual time

---

### 🔵 Privilege Escalation
- Event ID 4672 appears unexpectedly

---

## 🧠 What I Learned

- Windows logs are critical for authentication analysis
- Event IDs help quickly identify suspicious behavior
- Failed logins (4625) are key indicator of attacks

---

## 🛠 Tools
- Splunk (for analysis)
