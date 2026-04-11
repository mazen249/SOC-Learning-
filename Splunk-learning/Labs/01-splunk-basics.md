## 📌 Objective
Learn the fundamentals of Splunk and how to analyze logs using basic SPL queries.

---

## 🧠 What I Learned
- Searching logs using index and sourcetype
- Filtering web traffic logs
- Using stats and timechart for analysis
- Identifying suspicious user agents
- Understanding firewall logs and data transfer

---

## 🛠 Commands Used

```spl
index=main sourcetype=web_traffic

index=main sourcetype=web_traffic | timechart span=1d count

index=main sourcetype=web_traffic user_agent!=*Mozilla* user_agent!=*Chrome* user_agent!=*Safari*

sourcetype=firewall_logs src_ip="10.10.1.5" action="ALLOWED" | stats sum(bytes_transferred) by src_ip
