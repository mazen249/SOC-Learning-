# 📊 Introduction to SIEM 

---

## 📌 Overview

SIEM (Security Information and Event Management) is a security solution that collects logs from all devices in a network, normalizes their format, correlates events, and detects threats using detection rules.

---

## 🧠 Why SIEM?

| Problem | SIEM Solution |
|---------|---------------|
| Logs scattered across many devices | Centralized Log Collection |
| Different log formats (Windows, Linux, Firewall) | Normalization |
| Individual logs lack context | Correlation |
| Massive volume of logs | Real-time Alerting |
| Hard to track security status | Dashboards & Reporting |

---

## 🔧 Core Features of SIEM

| Feature | Description |
|---------|-------------|
| **Centralized Log Collection** | Collects logs from all sources (endpoints, servers, firewalls) via agents, APIs, or syslog |
| **Normalization** | Parses logs into fields and converts all logs to a consistent format |
| **Correlation** | Links events from different sources to identify attack patterns |
| **Real-time Alerting** | Triggers alerts based on detection rules |
| **Dashboards & Reporting** | Visualizes data and provides actionable insights |

---

## 📂 Log Sources

### Host-Centric Logs (device-focused)

| Source | Example Logs |
|--------|--------------|
| Windows | Event ID 4625 (failed login), 4688 (process creation) |
| Linux | `/var/log/auth.log`, `/var/log/syslog`, `/var/log/cron` |
| Web Server | Apache / Nginx access and error logs |

### Network-Centric Logs (traffic-focused)

| Source | Example Logs |
|--------|--------------|
| Firewall | Allowed/Blocked connections |
| Router | VPN connections, NAT logs |
| IDS/IPS | Intrusion alerts |

---

## 📥 Log Ingestion Methods

| Method | Description |
|--------|-------------|
| **Agent / Forwarder** | Lightweight tool installed on endpoint (e.g., Splunk Universal Forwarder) |
| **Syslog** | Standard protocol for sending logs from network devices |
| **Manual Upload** | Upload offline logs (CSV, log files) for analysis |
| **Port-Forwarding** | SIEM listens on a port, endpoints forward data to it |

---

## ⚙️ Detection Rules

Rules are logical conditions that trigger alerts.

| Example Rule | Alert |
|--------------|-------|
| 5 failed logins in 10 seconds | Multiple Failed Login Attempts |
| Successful login after multiple failures | Successful Login After Brute Force |
| USB device plugged | USB Device Detected |
| Outbound traffic > 25 MB | Potential Data Exfiltration |


