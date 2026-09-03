# Cybersecurity Portfolio

Welcome to my cybersecurity portfolio! This repository showcases hands-on experience in **vulnerability assessments**, **web application penetration testing**, **network traffic analysis**, **incident response**, and **threat modeling**. 

The projects included here reflect practical scenarios and frameworks completed through a **Virtual Cybersecurity Internship** and the **Google Cybersecurity Professional Certificate**.

---

## 🛠️ Technical Skills & Tools

* **Network Analysis & Recon:** `Wireshark`, `tcpdump`, `Nmap`, Port Scanning, Packet Capture Analysis (`.pcapng`), ICMP/DNS/HTTP Protocols[cite: 2, 5, 6, 8]
* **Web Security & Pentesting:** `Burp Suite` (Proxy, Intruder, Repeater), `OWASP ZAP`, `Nikto`, SQL Injection (SQLi), Cross-Site Scripting (XSS), Command Injection, LFI, CSRF, Broken Access Control[cite: 1, 3]
* **Security Frameworks & Standards:** NIST CSF, NIST SP 800-30 Rev. 1, PASTA Threat Modeling, PCI-DSS, OWASP Top 10, `MITRE ATT&CK`, CVE/CVSS[cite: 1, 2, 4, 7, 9]
* **Incident Response & SIEM:** Log Analysis, Phishing Escalations, Malware Triage (`VirusTotal`), DDoS Mitigation, SIEM/IDS Alerting[cite: 5, 9, 10]
* **Operating Systems & Environments:** Linux CLI, MySQL Database Administration, Virtual Lab Environments (DVWA, OWASP Juice Shop)[cite: 1, 3, 7]

---

## 📁 Repository Structure
```text

cybersecurity-portfolio/
├── README.md
├── assets/
│   └── images/
├── 01-virtual-internship/
│   ├── README.md
│   ├── task-2-networking-recon/
│   ├── task-3-vulnerability-assessment/
│   └── task-4-web-app-security/
└── 02-google-cybersecurity/
    ├── README.md
    ├── threat-modeling-pasta/
    ├── vulnerability-assessments/
    └── incident-response/

```
---

## 🚀 Projects Overview

### 01. Virtual Cybersecurity Internship

* **[Task 2: Networking, Reconnaissance & Traffic Analysis](./01-virtual-internship/task-2-networking-recon/)**
  * Performed network discovery and service identification using `Nmap` (`-sn`, `-sV`, `-O`, `-A`)[cite: 2].
  * Captured and analyzed ICMP/HTTP traffic packets with `Wireshark`[cite: 2].
  * Mapped threat actor tactics and vulnerabilities to CVE, CVSS, and the MITRE ATT&CK framework[cite: 2].

* **[Task 3: Web Vulnerability Assessment & Server Scanning](./01-virtual-internship/task-3-vulnerability-assessment/)**
  * Deployed OWASP Juice Shop locally and audited web traffic using `Burp Suite` (Proxy, Repeater, Intruder, Decoder)[cite: 1].
  * Executed web server scans using `Nikto` and identified critical findings like Authentication Bypass via SQLi and Broken Access Control[cite: 1].

* **[Task 4: Web Application Security & OWASP Top 10](./01-virtual-internship/task-4-web-app-security/)**
  * Configured DVWA (Low Security) to manually test and exploit SQLi, Reflected XSS, Command Injection, LFI (`/etc/passwd`), and CSRF[cite: 3].
  * Ran automated vulnerability scans using `OWASP ZAP` and intercepted HTTP requests via `Burp Suite`[cite: 3].

---

### 02. Google Cybersecurity Professional Certificate

* **[PASTA Threat Modeling Framework](./02-google-cybersecurity/threat-modeling-pasta/)**
  * Applied the 7-stage PASTA threat modeling methodology to an e-commerce sneaker application[cite: 4].
  * Defined API security boundary controls, data flow diagrams, threat trees, and risk mitigations (PCI-DSS compliance, SHA-256)[cite: 4].

* **[NIST SP 800-30 Vulnerability Assessment](./02-google-cybersecurity/vulnerability-assessments/)**
  * Conducted a formal risk assessment for a Linux/MySQL database server environment following NIST SP 800-30 Rev. 1[cite: 7].
  * Evaluated threat sources, severity, and likelihood, recommending remediation like TLS encryption and IP allow-listing[cite: 7].

* **[Incident Response & Traffic Analysis Journal](./02-google-cybersecurity/incident-response/)**
  * **Ransomware & Phishing Escalation:** Investigated phishing payloads (`bfsvc.exe`, hash `54e6ea...7f6b`), analyzed VirusTotal indicators, and generated L2 SOC escalation tickets[cite: 5, 10].
  * **DDoS Incident Mitigation:** Documented an ICMP flood response aligned with the NIST CSF lifecycle (Identify, Protect, Detect, Respond, Recover)[cite: 9].
  * **DNS & Malicious Redirection Analysis:** Diagnosed DNS UDP Port 53 unreachable errors and analyzed HTTP packet captures using `tcpdump` to trace unauthorized URL redirects (`greatrecipesforme.com`)[cite: 6, 8].

---

## 📜 Certifications & Verification

* **Google Cybersecurity Professional Certificate**
* **Virtual Cybersecurity Internship Certificate**

---

## 📬 Connect with Me

* **[LinkedIn:](https://www.linkedin.com/in/muhammad-uzair-j21/)**
* **Email: uzair.jay@gmail.com**

---