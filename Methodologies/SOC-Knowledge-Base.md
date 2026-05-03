# 🛠 شرح أدوات SOC الأساسية

---

## 🌐 Wireshark

<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/d/dc/Wireshark_Logo.svg" width="150"/>
</p>

📌 ما هو؟  
أداة لتحليل الشبكة.

⚙️ ماذا يفعل؟  
- يلتقط البيانات (Packets)  
- يحلل حركة الشبكة  
- يكشف الاتصالات المشبوهة  

🎯 استخدامه:  
تحليل الهجمات ومراقبة الشبكة

---

## 🛡 Wazuh

<p align="center">
<img src="https://wazuh.com/uploads/2020/04/wazuh_logo.svg" width="150"/>
</p>

📌 ما هو؟  
نظام SIEM للمراقبة الأمنية.

⚙️ ماذا يفعل؟  
- يجمع اللوق (Logs)  
- يحلل الأحداث  
- يصدر تنبيهات  

🎯 استخدامه:  
اكتشاف الهجمات وتحليلها

---

## 🖥 Sysmon

<p align="center">
<img src="https://learn.microsoft.com/en-us/sysinternals/media/sysmon/sysmon.png" width="150"/>
</p>

📌 ما هو؟  
أداة من مايكروسوفت لمراقبة نظام ويندوز.

⚙️ ماذا يفعل؟  
- يسجل تشغيل البرامج  
- يراقب النشاط داخل الجهاز  

🎯 استخدامه:  
كشف السلوك الخبيث

---

## 🤖 Shuffle (SOAR)

<p align="center">
<img src="https://shuffler.io/images/logo.png" width="150"/>
</p>

📌 ما هو؟  
منصة أتمتة أمنية (SOAR).

⚙️ ماذا يفعل؟  
- يستقبل التنبيهات من Wazuh  
- ينفذ إجراءات تلقائية  

🎯 استخدامه:  
تسريع الاستجابة للحوادث الأمنية

---

## 🐳 Docker

<p align="center">
<img src="https://www.docker.com/wp-content/uploads/2022/03/vertical-logo-monochromatic.png" width="120"/>
</p>

📌 ما هو؟  
منصة لتشغيل التطبيقات داخل حاويات (Containers).

⚙️ ماذا يفعل؟  
- يشغل الأدوات بسهولة  
- يعزل البيئة  

🎯 استخدامه:  
تشغيل بيئة SOC مثل Wazuh

---

## 💣 Mimikatz

<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/2/2f/Hacker-icon.png" width="100"/>
</p>

📌 ما هو؟  
أداة يستخدمها المهاجمون.

⚙️ ماذا يفعل؟  
- يستخرج كلمات المرور من الذاكرة  

🎯 استخدامه:  
محاكاة هجمات Credential Access (T1003)

---

## 🔗 كيف تعمل الأدوات معًا
Sysmon → تسجيل الأحداث  
↓  
Wazuh → تحليل واكتشاف  
↓  
Shuffle → استجابة تلقائية  

---

## 🎯 الخلاصة

- Sysmon = تسجيل النشاط  
- Wazuh = تحليل وكشف  
- Shuffle = استجابة  
- Wireshark = تحليل الشبكة  
- Docker = تشغيل البيئة  
- Mimikatz = محاكاة الهجوم  

---
