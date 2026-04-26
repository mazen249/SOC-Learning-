# 🛡 Investigation 4 - Brute Force Attack (Account Lockout)

## 📌 Scenario
A simulated brute force attack was performed against a Windows user account to analyze authentication logs and system defenses.

---

## 📊 Failed Login Attempts (Event ID 4625)

![Failed Logins](../screenshots/failed.png)

Multiple failed login attempts were observed targeting the user account hacker.

### 🔍 Observations:
- Repeated authentication failures detected
- Indicates brute force attack activity

---

## 🔒 Account Lockout (Event ID 4740)

![Account Lockout](../screenshots/lockout.png)

The user account hacker was locked out after multiple failed login attempts.

### 🔍 Observations:
- Account lockout policy triggered
- Prevented further unauthorized access attempts

---

## 🧠 Analysis

The sequence of events clearly indicates a brute force attack:

1. Multiple failed login attempts (4625)
2. Account lockout triggered (4740)

This shows that the system successfully detected and blocked the attack.

---

## 🚨 Conclusion

The brute force attack was unsuccessful due to security controls.

This highlights the effectiveness of account lockout mechanisms in protecting user accounts.

---

## 🔴 Severity
Medium

---

## 🛠 Tools Used
- Windows Event Viewer 
