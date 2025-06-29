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

## What this does

"><script>alert(...) — DOM-XSS popup

<form action=...> — Reflection-XSS injects phishing form

Form submits to attacker-controlled site

---

The user will get popup prompting the user to log in first

![4](https://github.com/user-attachments/assets/c69b1a2e-450e-4671-a7b7-158655d13622)


---

from the injected Payload it ask the user to enter the username and password

![5](https://github.com/user-attachments/assets/680fb121-c1f9-44f4-acd2-a7703e54d0e6)


---


from the Attackers side I created a custom PHP Script (capture.php) which grabs the cred from the user:

![8](https://github.com/user-attachments/assets/d97c548c-4676-4e6f-bc8d-3b43598c6aec)


---

Saved the file and Started the PHP script

>  php -S 0.0.0.0:8000


---

for the login Creden i gave Tom:qwerty!


![9](https://github.com/user-attachments/assets/8bd4fefa-309e-43ab-819f-c35df2ff75e1)

---

from the Attackers side i was able to capture the users cred through hosted PHP host

![10](https://github.com/user-attachments/assets/425063a8-a439-486f-8c64-fd493cfa12d9)

---

Getting POST request from captured Details

![7](https://github.com/user-attachments/assets/32bcdb15-8614-4492-933f-edcf4a46f6ff)







