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

## 🏗️ Project Structure


## xss-demo-vulnerable-app/
## │
## ├── vulnerable-java-app/ # Java Spring web app (hosted on Tomcat)
## │ └── index.jsp, controller, etc.
## │
## ├── phishing-backend/ # PHP server to capture credentials
## │ └── capture.php
## │
## ├── screenshots/ # Demo flow (optional)
## │ └── phishing-demo.png
## │
## └── README.md
