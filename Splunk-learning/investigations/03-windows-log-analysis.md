# 🛡 Investigation 3 - Windows Log Analysis (Brute Force Check)

## 📌 Scenario
Analyzing Windows Security Logs using Event Viewer to detect potential brute force login attempts.

---

## 📊 Failed Login Attempts (Event ID 4625)

![Failed Logins](../screenshots/logon.png)

We filtered Windows Security Logs for Event ID 4625, which represents failed login attempts.

### 🔍 Observations:
- Only 2 failed login attempts were recorded
- Account Name: MEZOOS
- Logon Type: 2 (Interactive login)

➡️ The number of failed attempts is very low and does not indicate brute force activity.

---

## 🔐 Successful Logins (Event ID 4624)

![Successful Logins](../screenshots/logon.png)

We analyzed Event ID 4624, which represents successful logins.

### 🔍 Observations:
- Normal login activity detected
- No suspicious login behavior

---

## 🚪 Logoff Activity (Event ID 4634)

![Logoff](../screenshots/logoff.png)

Event ID 4634 indicates user logoff.

### 🔍 Observations:
- Normal logoff activity for user sessions
- No abnormal session behavior detected

---

## 🔑 Privileged Logon (Event ID 4672)

![Privileges](../screenshots/privileges.png)

Event ID 4672 indicates special privileges assigned during logon.

### 🔍 Observations:
- The event was associated with the SYSTEM account
- This is expected behavior and not malicious

---

## 🧠 Analysis

During the investigation, we analyzed Windows authentication logs to identify potential attack patterns.

- Event ID 4625 showed only a small number of failed login attempts
- No repeated or automated login attempts were observed
- Event ID 4624 showed normal successful logins
- Event ID 4634 confirmed normal logoff behavior
- Event ID 4672 showed expected privileged activity from SYSTEM account

There was no correlation between failed attempts and suspicious successful logins.

---

## 🚨 Conclusion

No brute force attack was detected.

The observed activity represents normal user behavior.

---

## 🔴 Severity
Low

---

## 🛠 Tools Used
- Windows Event Viewer
