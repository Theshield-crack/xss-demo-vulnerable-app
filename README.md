# xss-demo-vulnerable-app

# XSS Demo: Vulnerable Java Web App + Credential Capture (Educational Lab)

This project demonstrates how **DOM-based and reflected Cross-Site Scripting (XSS)** vulnerabilities can be chained together to simulate a **phishing attack** using a vulnerable Java Spring web application and a credential-capturing PHP backend.

> ⚠️ **This project is intended solely for educational, ethical, and testing purposes. Do not deploy or use in any environment you do not own or have permission to test.**

---

## 🎯 Objective

To simulate how an attacker could:
1. Exploit a DOM-based and reflected XSS vulnerability.
2. Inject a fake login form into a web page.
3. Capture submitted credentials using a local PHP server.

---


I Started the webapp which is hosted in my localhost (Tomcat)


![1](https://github.com/user-attachments/assets/b31668e0-8e4f-45aa-8e8d-9cd6472808e8)


---

Next, i inerted a DOM based XSS script in the query 

![3](https://github.com/user-attachments/assets/0e58c723-c4f5-4fc5-9b75-03e9dd928f97)


Payload

![2](https://github.com/user-attachments/assets/9c7d843d-260e-42c5-9a17-9956de85868a)





